# Comparador de Orçamentos

Ferramenta para montar e comparar orçamentos de qualquer coisa — uma reforma,
uma viagem, um evento, a troca do carro. Cada linha é uma categoria e cada
célula uma cotação: clique numa cotação para escolhê-la e o total se ajusta
sozinho. Salve combinações diferentes e compare os cenários lado a lado.

É **um arquivo só** (`index.html`), sem build, sem dependências, sem servidor.
Dá para abrir com dois cliques no seu computador ou hospedar em qualquer lugar.

## Como usar

- **Escolher** uma cotação: clique nela. Clique de novo para desmarcar.
- **Editar / remover** uma cotação: botões ✎ e × dentro do quadrinho.
- **Adicionar** cotação ou categoria: botões pontilhados `+`.
- **Meta**: digite o valor no topo — a diferença fica verde (dentro) ou vermelha (acima).
- **Combinações salvas**: guarde um conjunto de escolhas com um nome e volte a
  ele depois com "Carregar". Ótimo para comparar cenários.
- **Exportar / Importar JSON**: para fazer backup ou levar os dados para outro
  navegador, celular ou computador.

O site começa vazio. Para trazer seus dados, use **Importar JSON**.

Nos campos de valor pode digitar do jeito que preferir: `11700`, `11.700`,
`1.234,56` ou até `R$ 11.700`.

> Os dados ficam salvos no `localStorage` do navegador — ou seja, só naquele
> navegador, naquele aparelho. Trocou de celular ou limpou os dados do site,
> os números somem. Por isso vale exportar o JSON de vez em quando.

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser público ou privado).
2. Suba o `index.html` (arraste o arquivo na página do repositório e faça commit).
3. No repositório: **Settings → Pages**.
4. Em *Source*, escolha **Deploy from a branch**; em *Branch*, `main` e pasta `/ (root)`. Salve.
5. Em um ou dois minutos o site aparece em
   `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

Pelo terminal, se preferir:

```bash
git init
git add index.html README.md
git commit -m "Comparador de orçamentos"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
git push -u origin main
```

Depois é só ligar o Pages no passo 3 acima.

### Outras opções igualmente simples

Como é um arquivo estático, funciona sem alteração nenhuma em:

- **Netlify Drop** (<https://app.netlify.com/drop>) — arraste a pasta, sai no ar na hora.
- **Cloudflare Pages**, **Vercel** — conecte o repositório e publique.
- Qualquer hospedagem que sirva HTML.

## Privacidade

O `index.html` **não contém nenhum dado seu** — o site começa zerado e tudo o
que você digitar fica só no seu navegador. Então pode subir num repositório
público sem preocupação. O único arquivo com informação sensível é o JSON que
você exporta; esse **não** suba para o GitHub.

## Personalizar

Tudo está em `index.html`:

- **Cores** — no bloco `:root` do CSS, lá em cima (`--accent` é o laranja).
- **Textos** — direto no HTML (título, subtítulo, rodapé).
