# Trabalho Individual - GCES - 2020/1

## 1. Containerização

A conteinerização da aplicação foi feita com a utilização das ferramentas Docker (v19.03.13) e Docker Compose (v1.26.0, com sintaxe na versão 3.8). 

Para rodar localmente a aplicação, utilize o comando:

`docker-compose up --build`

Concluído o processo, basta acessar o endereço `localhost:8080` para ter acesso às funcionalidades do sistema.

## 2. Integração Contínua

A integração contínua foi configurada com o auxílio da ferramenta GitlabCI. Quatro _jobs_ foram definidos no pipeline, sendo um para o processo de _build_ da aplicação e três para o processo de testes. 

Os três _jobs_ que compõem o processo de teste foram definidos da seguinte maneira:

* **api_test:** execução dos testes da api desenvolvida em Ruby on Rails;
* **web_test:** execução dos testes do frontend desenvolvido em Vue.js;
* **code_quality:** geração de métricas de qualidade de código, com a utilização da configuração default do Code Climate (o arquivo codeclimate.html pode ser baixado na página de execução do _job_ no Gitlab).
