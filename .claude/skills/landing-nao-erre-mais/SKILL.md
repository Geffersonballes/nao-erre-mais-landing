---
name: landing-nao-erre-mais
description: Guia de identidade visual, estrutura, copy e publicação da landing page do Método Não Erre Mais (Pedagogia • Conhecimentos Específicos, Prof. Romário Costa). Use em QUALQUER pedido que altere o visual, o texto, a estrutura, os preços, as seções ou a publicação desta landing (index.html deste repositório), e também ao criar outra página ou peça que deva seguir a mesma identidade.
---

# Landing — Método Não Erre Mais

Página de vendas do curso **Método Não Erre Mais: Pedagogia • Conhecimentos Específicos**, do **Prof. Romário Costa** (@prof.romariocosta). Curso para professores que vão prestar concurso: pílulas de microaprendizagem em vídeo + simulado com Inteligência Artificial que descobre onde o aluno erra e treina até acertar.

- **Arquivo:** `index.html` (arquivo único: HTML + CSS + JS, sem build)
- **No ar:** https://naoerremais.ballestech.com.br (GitHub Pages, branch `main`)
- **Repositório:** https://github.com/Geffersonballes/nao-erre-mais-landing

## REGRA DE OURO: esta skill aprende

**Toda instrução do usuário que mude visual, forma, texto, estrutura, preço ou regra da página deve ser registrada aqui**, na mesma alteração que a aplica:

1. Aplique a mudança no `index.html`.
2. Atualize a seção correspondente desta skill (tokens, seções, copy, regras) para refletir o estado novo.
3. Acrescente uma linha no **Registro de decisões** (fim do arquivo), com data, o que foi pedido e o porquê, se o usuário disse.
4. Faça commit da página e da skill juntas.

Se uma instrução nova contradiz uma regra antiga, a nova vale: atualize a regra e registre a troca no log. Nunca deixe a skill descrever algo que a página já não faz.

## Identidade visual

**Direção:** fundo claro creme + estilo tecnológico/IA com interação (inspirado em landings de SaaS escuras com feixes de luz neon, fluxograma animado, rótulos em fonte de código e títulos que saem do desfoque), mas com fundo claro. Três "ilhas" escuras em azul-marinho dão contraste: o card do fluxo da IA no topo, a seção das 26 pegadinhas e o card da oferta.

### Tokens (`:root` = claro; `.dark` = ilhas azul-marinho)

| Token | Claro | `.dark` | Uso |
|---|---|---|---|
| `--bg` / `--bg2` | `#FBF6EE` / `#F3EADB` | `#14213D` / `#1A2A4C` | fundos |
| `--text` / `--muted` | `#14213D` / `#5B6478` | `#EEF1F6` / `#A3ACC0` | texto |
| `--accent` | `#0B7C47` (verde escuro) | `#E4FF52` (neon) | texto de destaque, eyebrows, itálicos |
| `--cta` / `--cta-text` | `#12A15E` / `#fff` | `#E4FF52` / `#0A0D05` | botões |
| `--yellow` | `#FFE14D` | igual | marca-texto, selos de bônus/economia |
| `--red` | `#FF5A47` | igual | erros, "Reforçar", preço riscado |
| `--orange` | `#FE772B` | igual | Módulo 1 (cor das capas de Tendências) |
| `--green` | `#22C878` | igual | Módulo 2, "Dominado" |

Para criar uma ilha escura, adicione a classe `dark` ao elemento: os tokens trocam sozinhos.

### Tipografia (Google Fonts)

- **Títulos:** Poppins 900, **CAIXA ALTA** (`h1`, `h2`)
- **Palavra-chave em itálico:** Instrument Serif itálico (`<span class="it">`), em `--accent`, com marca-texto amarelo por baixo no claro. Uma por título.
- **Texto:** Inter
- **Rótulos técnicos** (eyebrows, status, logs, chips, metadados): JetBrains Mono, minúsculas

### Marca

- Selo **"NÃO ERRE MAIS!"**: fundo branco, borda e texto vermelhos, inclinado −3° (`.stamp`)
- Tarja verde **"PEDAGOGIA • CONHECIMENTOS ESPECÍFICOS"**
- Logo da barra: quadrado verde com ✓ + "NÃO ERRE MAIS"

### Componentes

- `.glass` card branco translúcido com sombra; `.spot` luz que segue o cursor
- `.btn` CTA verde com brilho passando; `.btn-ghost` secundário
- `.eyebrow` rótulo mono com ponto pulsante
- `.tag` `.t-grn` / `.t-yel` / `.t-red` = Dominado / Em evolução / Reforçar
- `.bonus-tag` selo amarelo com borda e sombra azul-marinho
- `.ph` marcador amarelo tracejado para dados pendentes (`[PREENCHER]`, `[CONFIRMAR]`)

### Interações (manter todas)

1. Linhas de luz em canvas no topo e na oferta (pausam fora da tela; mais suaves no celular)
2. Fluxo da IA em SVG com pontos percorrendo caminhos + log em tempo real
3. Títulos `.blur` aparecem palavra por palavra saindo do desfoque
4. Números `data-scr` embaralham antes de fixar
5. Mini simulado em formato de chat (digitando… → questão → feedback → diagnóstico)
6. Painel de evolução: barra do Wallon sobe de Reforçar → Em evolução → Dominado
7. Linha do tempo do "Como funciona" acende com a rolagem
8. Pegadinhas: tocar para revelar o macete
9. Calculadora de ritmo (slider de minutos por dia)
10. Apostila: páginas empilhadas para folhear, arrastar e ampliar (lightbox)
11. Borda de luz girando no card da oferta; barra de progresso no topo; CTA fixo no celular

Sempre respeitar `prefers-reduced-motion` e pausar animações fora da tela.

## Ordem das seções

1. Barra (logo, status "IA online • simulados ativos", botão Começar)
2. **Hero:** selo + tarja, pill mono, H1 *"Você não precisa estudar mais. Precisa parar de **errar** o que mais cai."*, subtítulo do simulado com IA, 4 checks, CTA + "Testar 5 pegadinhas grátis", preço; à direita o card escuro do fluxo da IA
3. Números: 13 pílulas • 26 pegadinhas • 120 questões no banco • 7 dias de garantia
4. Dor (4 cards) + frase de virada
5. Comparação: banco de questões comum × Método Não Erre Mais
6. Mini simulado grátis (5 questões)
7. Como funciona (5 passos) + painel de evolução
8. 26 pegadinhas (ilha escura)
9. Calculadora de ritmo
10. Módulos (01 laranja, 02 verde, "em produção")
11. Apostila — **BÔNUS** (páginas para folhear)
12. Vídeo tutorial
13. Para quem é (3 perfis)
14. Professor (bio justificada, selos, citação, redes sociais)
15. Oferta (card escuro, caixa de bônus, preço) + garantia
16. FAQ
17. Chamada final + rodapé (redes, aviso de que não garante aprovação)

## Conteúdo e regras de copy

- **Promessa central:** "Você não precisa estudar mais. Precisa parar de errar o que mais cai." e "O simulado com IA que descobre onde você erra e treina você até acertar." Tom forte, em caixa alta nos títulos.
- **Nunca prometer aprovação ou resultado garantido** ("nunca mais vai errar", "passe garantido"). O tom é forte, mas sobre o método.
- **Não citar bancas pelo nome.** Dizer "questões de bancas reais". Foco do curso: Mato Grosso, mas a página não restringe o público por estado.
- **Nunca inventar** depoimentos, números de alunos ou resultados. Faltou dado real → marcador `.ph`.
- Preço riscado só se for um valor real; questões do mini simulado são demonstrativas e a página avisa isso.
- Frases literais do Romário (da transcrição das aulas) são preferidas a frases inventadas.

### Dados do curso

- **Preço:** de ~~R$ 147~~ por **R$ 47 à vista** ou **5x de R$ 9,40**. Garantia de 7 dias. Venda pela Hotmart.
- **Módulo 01 — Tendências Pedagógicas** (8 eps, ~12 min): Mapa Geral Liberais × Progressistas; Liberal Tradicional; Renovada Progressivista (Escola Nova); Renovada Não-Diretiva (Carl Rogers); Liberal Tecnicista (Skinner); Progressista Libertadora (Paulo Freire); Progressista Libertária; Crítico-Social e Histórico-Crítica (Saviani).
- **Módulo 02 — Teorias da Aprendizagem** (5 eps, ~10 min): Piaget; Vygotsky; Wallon; Ausubel; Ciclos de Vida Humana.
- **Em produção:** Avaliação da Aprendizagem; Currículo e Didática.
- **Simulado:** 10 questões sorteadas do banco do módulo (70 em Tendências, 50 em Teorias), com explicação em cada uma; o sorteio prioriza as que o aluno não viu; painel com meta de 70%.
- **Bônus:** apostila de aprofundamento em PDF do Módulo 1 (20 páginas, 8 capítulos, 16 questões comentadas, pegadinhas, curiosidades, quadro comparativo, linha do tempo). Base: Libâneo, Saviani, Paulo Freire, Carl Rogers.
- **Professor:** Romário Costa — professor pedagogo; pós-graduado em Ensino Híbrido; graduado em Tecnologia Educacional (UFMT); formador de professores (rede municipal de Sapezal, MT); especialista em IA na personalização do ensino e da aprendizagem; criador do treinamento *Aulas Engajadoras*; músico, compositor, guitarrista, produtor audiovisual e musical. Citação: "O conhecimento é um lugar, e nós, professores, somos os guias que mostram o caminho para se chegar até ele."
- **Redes:** Instagram e TikTok @prof.romariocosta; YouTube @engajadamente. Só na seção do professor e no rodapé (nunca perto dos CTAs).

### Pendências (atualizar quando o usuário enviar)

- [ ] Foto do Romário (`[FOTO DO PROF. ROMÁRIO AQUI]`)
- [ ] `CHECKOUT_URL` da Hotmart (fim do `<script>`)
- [ ] `VIDEO_ID` do vídeo tutorial no YouTube
- [ ] Tempo de acesso (FAQ)
- [ ] Confirmar: R$ 147 é preço real; 5x sem juros; módulos e apostilas futuros sem custo extra; banco de 120 questões

## Fluxo de trabalho técnico

1. Editar `index.html` (CSS em `<style>`, JS em `<script>`; imagens da apostila em base64 webp).
2. Testar com Playwright em **375 px** e **1280 px**: sem erros no console e `scrollWidth` igual à largura da janela (nada vazando na lateral). Tirar print das seções alteradas e olhar.
3. Atualizar esta skill (regra de ouro acima).
4. Commit em português, explicando o que mudou, e `git push origin main`.
5. Conferir no ar: `curl -s https://naoerremais.ballestech.com.br | grep -q '<trecho novo>'`. Publica em 1 a 2 minutos. **Se não publicar**, o GitHub às vezes não dispara o build: envie um commit vazio (`git commit --allow-empty -m "Republica o site no GitHub Pages"`) e confira de novo.

### Domínio

- `CNAME` no repositório: `naoerremais.ballestech.com.br`
- DNS na Hostinger (`ballestech.com.br`): `CNAME naoerremais → geffersonballes.github.io`. **Nunca alterar** os registros de e-mail (MX, SPF, DKIM, autodiscover/autoconfig) nem os de verificação do Google.
- Quando comprarem o domínio do curso: trocar o `CNAME`, criar o registro no DNS novo e atualizar em *Settings → Pages*.

## Registro de decisões

| Data | Decisão |
|---|---|
| 2026-11-18 | Promessa sem garantia de resultado; frase principal "Você não precisa estudar mais…" em caixa alta no topo |
| 2026-11-18 | Destaque para o simulado com IA que adapta o estudo; questões de bancas reais; acesso pelo celular via Hotmart |
| 2026-11-18 | Página interativa no estilo tecnológico da referência (vídeo "Relay"): feixes de luz, fluxograma, mono, títulos com desfoque |
| 2026-11-18 | Fundo escuro rejeitado: voltar ao claro mantendo todas as interações; três ilhas escuras para contraste |
| 2026-11-18 | Apostila em PDF vira **BÔNUS**, separada das aulas; mapas mentais ficam para depois |
| 2026-11-18 | Não focar em uma banca; foco do curso é Mato Grosso, sem restringir o público na página |
| 2026-11-18 | Bio do professor atualizada; idade (39) fora da página por escolha de copy |
| 2026-11-18 | Redes sociais só na seção do professor e no rodapé; link do TikTok sem parâmetros de rastreamento |
| 2026-11-18 | Preço: de R$ 147 por R$ 47 à vista ou 5x de R$ 9,40, com selo "você economiza R$ 100" |
| 2026-11-19 | Texto da bio do professor **justificado**, com hifenização automática em português |
