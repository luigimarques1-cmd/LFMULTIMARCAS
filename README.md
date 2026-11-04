# LF MULTIMARCAS — Landing Page BLACK PREMIUM

Site estático responsivo (HTML, CSS e JavaScript), pronto para publicação no **GitHub e na Vercel**. Sem frameworks, build nem backend.

## O que foi alterado nesta versão

- **Novo banner vertical da LF Multimarcas** substitui o banner horizontal anterior e é exibido em destaque logo abaixo do cabeçalho com menu e lupa.
- O banner principal usa a **URL direta do ImageKit** enviada: https://ik.imagekit.io/verlcwgen/Jerseys%20em%20Destaque%20LF%20Multimarcas.png
- Suas dimensões originais são **1086 × 1448 px (proporção 3:4 vertical)**. A imagem é exibida inteira, sem cortes, com largura máxima de 680 px no computador e responsiva no celular.
- Botão flutuante do WhatsApp aponta para **+55 (47) 99628-5878**, número exibido no banner: `https://wa.me/5547996285878`.
- A identidade visual e o título foram atualizados para **LF MULTIMARCAS**; o Instagram **@lf.multimarcas98** está presente no próprio banner.
- Mantidos os **9 banners das ligas**, **187 clubes/seleções**, URLs de escudos da última lista, links dos catálogos, carrosséis com setas premium, menu, pesquisa e diagnóstico de escudos.
- Mantidos os escudos maiores: círculos de **92 px** em mobile, **118 px** intermediário e **138 px** em desktop.

**Hospedagem:** o banner é servido pelo ImageKit, sem necessidade de enviar a imagem principal ao repositório. Se a URL externa sair do ar, o banner também deixará de aparecer; mantenha o arquivo publicado no ImageKit.

## Arquivos

```text
index.html                      Página principal
style.css                       Visual responsivo e botão flutuante
script.js                       Navegação, pesquisa, carrosséis e contato
configuracao.js                 Dados da loja, banners e clubes
diagnostico-escudos.html        Ferramenta de verificação dos escudos
diagnostico-escudos.js          Lógica do diagnóstico
relatorio-escudos-atualizados.txt  Histórico de alterações de URLs
assets/imagens/favicon-lf.png   Ícone do navegador
README.md                       Este manual
```

## Como substituir o projeto no GitHub conectado à Vercel

1. Extraia o ZIP no computador.
2. Abra o repositório do GitHub que já está conectado à Vercel.
3. Faça upload do **conteúdo da pasta extraída**, mantendo as subpastas. Substitua arquivos existentes com o mesmo nome.
4. Remova arquivos antigos desnecessários, especialmente `estilo.css` caso esteja no repositório antigo: o arquivo utilizado nesta versão é **`style.css`**.
5. Faça **Commit changes** na branch que sua Vercel acompanha (geralmente `main` ou `principal`).
6. A Vercel deverá iniciar um novo deploy automaticamente se a integração estiver ativa. Confira **Deployments** para confirmar.

Para um repositório novo: use `https://vercel.com/new`, importe o repositório, `Framework Preset: Other`, `Build Command: vazio`, `Root Directory: ./` e faça Deploy. Também funciona no GitHub Pages (publicando a raiz do repositório).

## Personalização para outros clientes

As URLs e os nomes são controlados em `configuracao.js`.

```js
loja: {
  nome: 'LF MULTIMARCAS',
  logo: 'https://ik.imagekit.io/verlcwgen/Jerseys%20em%20Destaque%20LF%20Multimarcas.png',
  whatsapp: '5547996285878',
  instagram: '@lf.multimarcas98'
}
```

Para trocar o banner, altere apenas `loja.logo` em `configuracao.js`. Se o novo arquivo tiver outra proporção, ajuste também `aspect-ratio` em `.featured-brand img` no `style.css`.

**Os banners dos campeonatos continuam com a proporção original 135:76 (1080 × 608 px).** O novo formato 3:4 aplica-se apenas ao banner principal da loja.

## Observações

- Cinco clubes continuam sem link de catálogo no arquivo original: **Genoa, Montpellier, Nantes, Brest e FC Dallas**. Esses nomes aparecem, mas não redirecionam para páginas inventadas.
- A disponibilidade das URLs públicas de escudos depende do servidor externo. Acesse `/diagnostico-escudos.html` na sua hospedagem para testar as imagens e baixar o relatório de possíveis falhas.
- Como os links dos catálogos abrem serviços externos, confira alguns exemplos depois do deploy.
- O número e o Instagram foram lidos da arte que você enviou; confirme que esses contatos continuam atualizados antes de divulgar.
