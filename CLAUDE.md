# Landing Método Não Erre Mais

Antes de qualquer alteração em `index.html` (visual, texto, estrutura, preço, seções ou publicação), carregue a skill **landing-nao-erre-mais** (`.claude/skills/landing-nao-erre-mais/SKILL.md`) e siga-a.

Toda instrução do usuário que mude o visual ou a forma da página também deve ser registrada nessa skill, na mesma alteração e no mesmo commit, para que ela continue descrevendo a página como ela é.

Responda ao usuário em português do Brasil.

## Equipe de subagentes (`.claude/agents/`)

A sessão principal conversa com o usuário, decide e delega:

| Subagente | Quando usar |
|---|---|
| `copywriter-nao-erre-mais` | O que a página diz: títulos, textos, oferta, FAQ, bio |
| `designer-interacoes` | Como a página parece ou se comporta: visual, animações, seções novas |
| `conteudo-curso` | Chegou material do curso (PDF, áudio, vídeo, Drive) para extrair dados e frases |
| `qa-publicacao` | Testar, auditar e publicar (commit, push, conferir no ar) |

Regras de orquestração:
- Copywriter e designer podem rodar em paralelo só quando mexem em seções diferentes; se a mesma seção estiver envolvida, rode um depois do outro.
- Subagentes de edição não fazem commit. A sessão principal revisa o resultado e pede ao `qa-publicacao` para testar e publicar.
- O que um subagente relatar como decisão ou pedido novo do material deve ser confirmado com o usuário antes de virar regra na skill.
- Ao delegar a publicação, passe ao `qa-publicacao` as linhas de atribuição de commit desta sessão.
