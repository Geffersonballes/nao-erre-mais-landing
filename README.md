# Método Não Erre Mais — Landing Page

Página de vendas do curso **Método Não Erre Mais: Pedagogia • Conhecimentos Específicos**, do Prof. Romário Costa (@prof.romariocosta).

Microaprendizagem + simulado com Inteligência Artificial para concursos de professor.

## Estrutura

```
index.html                  → a landing page (arquivo único: HTML + CSS + JS)
versoes-anteriores/         → versões antigas, só para consulta
```

A página não depende de build nem de framework. Basta abrir o `index.html` no navegador.

## O que trocar antes de publicar

No fim do `index.html`, dentro do `<script>`:

```js
const CHECKOUT_URL = "#oferta";   // cole o link do checkout da Hotmart
const VIDEO_ID = "";              // ID do vídeo tutorial no YouTube
```

Busque também por `[PREENCHER]`, `[CONFIRMAR]` e `[FOTO DO PROF. ROMÁRIO AQUI]` no arquivo.

## Pendências

- [ ] Foto do Prof. Romário
- [ ] Link do checkout da Hotmart
- [ ] Vídeo tutorial no YouTube
- [ ] Tempo de acesso ao curso
- [ ] Confirmar: novos módulos (e suas apostilas) sem custo extra para quem já comprou
- [ ] Confirmar: banco com 120 questões (70 Tendências + 50 Teorias)

## Publicação

- **Endereço:** https://naoerremais.ballestech.com.br
- **Hospedagem:** GitHub Pages (branch `main`, pasta raiz). Cada envio para `main` atualiza o site em 1 a 2 minutos.
- **Domínio:** o arquivo `CNAME` aponta o Pages para o subdomínio. No DNS da Hostinger (`ballestech.com.br`) existe o registro `CNAME naoerremais → geffersonballes.github.io`.
- **Trocar de domínio no futuro:** altere o arquivo `CNAME`, crie o registro equivalente no DNS do novo domínio e atualize o domínio em *Settings → Pages*.

## Recursos da página

- Fluxo animado da IA (SVG) e linhas de luz (canvas)
- Mini simulado interativo em formato de chat, com diagnóstico
- Pegadinhas para tocar e revelar
- Calculadora de ritmo de estudo
- Apostila (bônus) com páginas para folhear e ampliar
- Respeita `prefers-reduced-motion`; animações pausam fora da tela
