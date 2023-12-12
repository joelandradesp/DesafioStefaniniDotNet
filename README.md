# Desafio para candidatos da Stefanini

## 1. Estudo de Caso

![Modelagem.](/DesafioStefaniniDotNet/ImagensREADME/Modelagem.jpg "Modelagem.")

O desafio é criar um porjeto back-end API em .NET Core 6.0, onde deverá ser desenvolvido o CRUD de pedidos seguindo a modelagem de dados acima e consistindo na base de dados SQL Server e como opcional a criação de um projeto front-end para integrar com a API.

## 2. Arquitetura

### 2.1 A api precisa ser entregue em .NET Core 6, podendo utilizar sua arquitetura de preferência, porem documentar como foi desenvolvida a arquitetura escolhida, e nesse cenário a arquitetura também será validada (DDD, SOLID, Clean Code e API REST é imprescindível). O front-end pode ser entregue com qualquer tipo de framework/lib javascript de qualquer versão (temos preferência a Angular e Vue.js).

## 3. Requisitos do ambiente

* Visual Studio 2022 ou Visual Studio Code;
* Banco de dados SQL, InMemory (detalhes abaixo) ou via Container (SQL Server).
    * Pode-se utilizar a lib do Entity Framework Core de banco de dados em memória oficial Microsoft.
    
Mais informações:

[Provedor de Banco de Dados na Memória do EF Core](https://learn.microsoft.com/pt-br/ef/core/providers/in-memory/?tabs=dotnet-core-cli)

## 4. Entregáveis

A não entrega do obrigatório o candidato será desclassificado e todos os artefatos precisam estar em um repositório GIT público com README detalhado do projeto e suas funcionalidades;

4.1. **Obrigatório**

* API.NET Core executando e com todas as API's funcionando;
* Swagger funcionando e configurado;
* ORM para comunicação com banco de dados;
    * POdendo ser utilizado o EF Core ou Dapper;
* Deve existir **APENAS** CRUD(GET, POST, PUT e DELETE) de **PEDIDOS. (Não tem CRUD de ItensPedido)**
* O GET de PEDIDO deve retornar o modelo de JSON:


4.2. **Desejável**

* Migration SQL funcionando no projeto;
* Frontend com todas as integrações e os comportamentos básicos funcionando;
* Link acessível com o projeto publicado na Azure/AWS/GCP;

![JSON.](/DesafioStefaniniDotNet/ImagensREADME/JSON.jpg) "JSON.")