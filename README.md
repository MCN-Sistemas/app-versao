# app-versao
app-versao

Repositório centralizado para armazenar configurações públicas dos aplicativos, como versão disponível, número do build e links para as lojas.

Estrutura

Cada projeto possui seu próprio diretório:

app-versao/
├── mcnfaturamento/
│   └── versao.json
├── outroprojeto/
│   └── versao.json
└── ...

Arquivo versao.json

Exemplo:

{
   "versaoAPP":"10.0.8",
   "versaoAPI":"2026.7.8.2", 
   "obrigatoria":false,
   "urlAndroid":"https://play.google.com/store/apps/details?id=com.mcnfaturamento.app&hl=pt_BR",
   "urlIOS":"https://apps.apple.com/br/app/faturamento/id6783046652"
}

Consulta

Os aplicativos podem consultar o arquivo diretamente através do GitHub Pages:

https://MCN-Sistemas.github.io/app-config/mcnfaturamento/versao.json

Exemplo em React Native / Expo:

const resposta = await fetch(
    "https://MCN-Sistemas.github.io/app-config/mcnfaturamento/versao.json"
);

const dados = await resposta.json();

Observação

Este repositório contém apenas informações públicas. Não armazenar senhas, tokens, chaves de API ou qualquer outra informação confidencial.