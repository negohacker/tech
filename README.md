# Suporte Hacker — GitHub Pages

Site estático para catálogo de softwares, drivers e links úteis. Não requer servidor backend, PHP, Node.js ou jQuery.

## Estrutura

- `index.html` — página principal na raiz do repositório.
- `data.json` — catálogo inicial de softwares e drivers.
- `assets/styles.css` — estilos responsivos, variáveis de tema e modo claro/escuro.
- `assets/app.js` — lógica em módulo ES.

## Publicar no GitHub Pages

1. Extraia os arquivos deste ZIP.
2. Envie `index.html`, `data.json` e a pasta `assets/` para a raiz do repositório GitHub.
3. No GitHub, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**, escolha a branch (por exemplo, `main`) e a pasta **/(root)**.
5. Salve e aguarde a publicação.

Os caminhos para recursos são relativos (`./assets/...` e `./data.json`), então funcionam também em repositórios publicados como `usuario.github.io/nome-do-repositorio/`.

## Atualizar o catálogo

Use a aba **Editor** para cadastrar, editar ou remover itens. O editor guarda o rascunho no armazenamento local do navegador. Clique em **Exportar data.json** e substitua o `data.json` no repositório para que as mudanças sejam publicadas para todos.

## Antes de publicar

- Revise os links e versões do catálogo; os links de download originais podem ter mudado ou ser temporários.
- No arquivo `assets/app.js`, altere `suporte@tech.com.br` para o endereço real de atendimento.
- A seção de contato original continha dados demonstrativos; esta versão não publica telefone ou endereço físico inventados.
- O modo estático não oferece autenticação: a aba Editor é apenas uma ferramenta local e não altera diretamente o repositório.
- Para testar `fetch("./data.json")`, use GitHub Pages ou uma extensão/servidor local simples no editor. Abrir `index.html` diretamente via `file://` pode bloquear a leitura de JSON por políticas do navegador.
