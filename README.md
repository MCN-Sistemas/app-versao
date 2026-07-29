# app-versao

Repositório centralizado para armazenar configurações públicas dos aplicativos, como versão disponível e links para as lojas.

## Estrutura

Cada projeto possui seu próprio diretório:

```text
app-versao/
├── mcnfaturamento/
│   └── versao.json
├── outroprojeto/
│   └── versao.json
└── ...
```

## Arquivo `versao.json`

Exemplo:

```json
{
  "versaoAPP": "10.0.8",
  "versaoAPI": "2026.7.8.2",
  "obrigatoria": false,
  "urlAndroid": "https://play.google.com/store/apps/details?id=com.mcnfaturamento.app&hl=pt-BR",
  "urlIOS": "https://apps.apple.com/br/app/faturamento/id6783046652"
}
```

## Consulta

Os aplicativos podem consultar o arquivo diretamente através do GitHub Pages:

```text
https://mcn-sistemas.github.io/app-versao/mcnfaturamento/versao.json
```

## Exemplo em React Native

```tsx
const resposta = await fetch(
  "https://mcn-sistemas.github.io/app-versao/mcnfaturamento/versao.json"
);

const dados = await resposta.json();

console.log(dados);
```

## Observação

Este repositório contém apenas informações públicas utilizadas pelos aplicativos.

Não armazenar senhas, tokens, chaves de API ou qualquer outra informação confidencial.
