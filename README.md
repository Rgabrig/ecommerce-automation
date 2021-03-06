## Sobre este projeto (Ecommerce Automation)

O intuito do projeto é realizar a automação de um processo onde o cliente irá acessar o e-commerce, filtrar os produtos como desejado e finalizar sua compra com sucesso. Validando os cenários necessários.

## Instalação e configuração

Para iniciar o projeto realize o comando ```cucumber --init``` dentro da pasta raiz para que assim a ferramenta gere as pastas necessárias para iniciar.

Dentro da pasta raiz crie um arquivo gemfile que será necessário para referenciar o projeto e instalar todas as gems necessárias para o mesmo rodar.

Após seleção das gems necessárias, utilize o comando ```bundle install``` para instalar todas as gems.

No seu arquivo ```env.rb``` descreva os requires necessários para utilizar no projeto, após isso, iremos realizar a configuração do Capybara para rodar no navegador desejado e também com as especificações desejadas.

> Gems utilizadas no projeto: Capybara, Cucumber, Selenium-Webdriver, Rspec, Site Prism

## Rodando o Projeto

Após instalação completa, podemos criar variáveis para rodar features especificas.

```
Exemplo:

Funcionalidade: Realizar login

@login
Cenario: Realizar login com sucesso
Quando eu realizo o login
Entao eu verifico se o login foi realizado com sucesso
```

Neste exemplo ao rodar o comando ```cucumber -t@login``` irei rodar apenas o teste login ao invés de todos os cenários escritos na pasta do projeto.
> Para executar o teste desse projeto basta utilizar o comando ```cucumber``` isto fará com que todos os testes sejam executados.

## Conceitos utilizados

Para melhor rendimento, foi utilizado no projeto o conceito de Page Objects e também alguns arquivos foram criados, como:
```page_helper.rb``` Neste arquivo deixo criado um modulo global onde já deixo minhas classes instanciadas para evitar retrabalho.
```cucumber.yml``` Neste arquivo configuro o formato para rodar os testes e crio a váriavel ENVIRONMENT para selecionar qual ambiente o teste irá rodar.
```qa.yml``` Neste arquivo deixo configurado o ambiente de QA para rodar meus testes, podendo ser criados mais arquivos com outros ambientes e quando necessário rodar o testes é só trocar a váriavel ENVIRONMENT.

PS: É necessário que no seu arquivo ```env.rb``` seja setado sua váriavel ENVIRONMENT e também o modulo criado no ```page_helper.rb``` como global.

Obs: No código foram incluidos alguns ```sleep(2)``` para facilitar a visualização do que está sendo feito. 

Se chegou até aqui, deixo meu agradecimento!!!
