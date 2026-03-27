# Git Actions
Repositório criado para estudos de Github Actions

# 1: Fluxo de trabalho de Integração Contínua (CI) para Node.js

Este fluxo de trabalho é acionado a cada push ou pull request para a branch master. Ele define um trabalho chamado "construir" que é executado em um ambiente Ubuntu. O trabalho usa a versão 14.x do Node.js, instala as dependências do projeto com npm ci, executa o script de build (se presente) com npm run build --if-present, e executa os testes com npm test.

# 2: Fluxo de trabalho para implantar no Heroku

Este fluxo de trabalho é acionado a cada push para a branch master. Ele define um trabalho chamado "implantar" que é executado em um ambiente Ubuntu. O trabalho faz checkout do código do repositório e, em seguida, usa a ação Heroku Deploy para implantar o aplicativo no Heroku. A ação Heroku Deploy usa a chave da API do Heroku, o nome do aplicativo e o e-mail que são fornecidos como variáveis de ambiente.

# 3: Fluxo de trabalho para implantar no Azure

Este fluxo de trabalho é acionado a cada push para a branch master. Ele define um trabalho chamado "construir-e-implantar" que é executado em um ambiente Ubuntu. O trabalho faz checkout do código do repositório, faz login no Azure usando o módulo Az e, em seguida, usa o comando az webapp up para implantar o aplicativo no Azure.

# 4: Fluxo de trabalho para implantar no AWS

Este fluxo de trabalho é acionado a cada push para a branch master. Ele define um trabalho chamado "implantar" que é executado em um ambiente Ubuntu. O trabalho faz checkout do código do repositório, configura as credenciais da AWS e, em seguida, usa o comando aws s3 sync para sincronizar o código do repositório com um bucket do S3.

# 5: Fluxo de trabalho de Integração Contínua (CI) para Python

Este fluxo de trabalho é acionado a cada push para o repositório. Ele define um trabalho chamado "construir" que é executado em um ambiente Ubuntu. O trabalho faz checkout do código do repositório, configura o Python 3.8, instala as dependências do projeto listadas no arquivo requirements.txt e, em seguida, executa os testes usando pytest.
