# Desafio para candidatos da Stefanini

## 1. Estudo de Caso

![Modelagem.](/ImagensREADME/Modelagem.jpg "Modelagem.")

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

![JSON.](/ImagensREADME/JSON.jpg) "JSON.")

# 5. Quetionário

Após a entrega do desafio, colabore com a sua opnião: Responda o questionario clicando aqui (faltou o link).


# Desenvolvimento

## Passos para o Desafio da Stefanini:

1. Criei um Repositório público no meu GitHub: https://github.com/joelandradesp/DesafioStefaniniDotNet
	* SSH: git@github.com:joelandradesp/DesafioStefaniniDotNet.git
	
	![GitHub Desafio Stefanini Dot Net.](/ImagensREADME/GitHubDesafioStefaniniDotNet.png "GitHub Desafio Stefanini Dot Net.")
	
2. Instalação do Visual Studio 2022 Community Edition
	* Download: https://visualstudio.microsoft.com/pt-br/vs/community/
	
	![Download Visual Studio Community.](/ImagensREADME/DownloadVisualStudioCommunity.png "Download Visual Studio Community.")
	
3. Instalar .Net Core 6.
	Link: https://dotnet.microsoft.com/pt-br/download/dotnet/6.0
	Escolher Windows - x64.
	* A instalação do Visual Studio 2022 faz a instalação do .Net Core 8 e portanto tem que ser instalado a parte do .Net Core 6.
	
	![Download Net Core 6](/ImagensREADME/DownloadNetCore6.png "Download Net Core 6.")
	
4. Atualizar o Idioma do Visual Studio 2022 para Inglês.

	1. Executar novamente o instalador do Visual Studio:
	
	![Instalador Visual Studio.](/ImagensREADME/InstaladorVisualStudio.png "Instalador Visual Studio.")
	
	2. Confirme as primeiras definições do instalador clicando em Continuar:
	
	![Downloads Necessarios](/ImagensREADME/DownloadsNecessarios.png "Downloads Necessarios.")
	
	3. Aguardo enquanto o Visual Studio Installer realiza os downloads necessários:
	
	![Downloads Necessarios](/ImagensREADME/DownloadsNecessarios.png "Downloads Necessarios.")
	
	4. Clique agora em Modificar:
	
	![Modificar Instalacao](/ImagensREADME/ModificarInstalacao.png "Modificar Instalacao.")
	
	5. Vá até a guia Pacotes de idiomas:
	
	![Pacote de Idiomas](/ImagensREADME/PacotedeIdiomas.png "Pacote de Idiomas.")
	
	6. Marque o Inglês, ou outro de sua preferencia e clique em Modificar:
	
	![Modificar Idioma](/ImagensREADME/ModificarIdioma.png "Modificar Idioma.")
	
	7. Finalizada a atualização, abra seu Visual Studio, localize o menu Ferramentas e na sequencia clique em Opções:
	
	![Ferramentas Opcoes](/ImagensREADME/FerramentasOpcoes.png "Ferramentas Opcoes.")
	
	8. Vá até Configurações Internacionais:
	
	![Configuracoes Internacionais](/ImagensREADME/ConfiguracoesInternacionais.png "Configuracoes Internacionais.")
	
	9. Selecione o idioma de sua preferência e clique em Ok para confirmar a alteração:
	
	![Idioma Ingles Selecionado](/ImagensREADME/IdiomaInglesSelecionado.png "Idioma Ingles Selecionado.")

	Agora o Visual Studio está em Inglês.
	
5. Problemas com o Nuget

O Nuget esta para o ambiente .Net como o Maven esta para o Java.
Após instalar o Visual Studio, não me atentei que houve uma falha na instalação. O Nuget não estava configurado para buscar os pacotes da internet e sim do repositório local. O nuget.org não estava configurado.

Essa é a imagem de como estava (era a única opção), não tinha a configuração nuget.org:

![Nuget Local](/ImagensREADME/NugetLocal.png "Nuget Local.")

Esse tipo de problema é algo não previsto, demora para identificar a origem.

Adicionado nuget.org:

![Adicionado Nuget.org](/ImagensREADME/adicionadonugetorg.png "Adicionado Nuget.org.")

Agora conseguimos escolher o ambiente local do Nuget ou do repositório da Internet que é o Nuget.org:

![Escolha entre Nuget.org ou local](/ImagensREADME/Nugetorg.png "Escolha entre Nuget.org ou local.")

6. Criação do Projeto no Visual Studio.
	6.1 - Escolha do Template
	O template escolhido foi o "ASP.NET Core Web API.

![Template Escolhido](/ImagensREADME/templateescolhido.png "Template Escolhido.")

Foi escolhido esse template, pois já tem o OpenAPI que é uma implementação do Swagger que é exigido no teste.

6.2. - Nome do Projeto: DesafioStefaniniCrudPedidos
	* Ficou o Path local: F:\DEsafioStefaniniDotNet\DesafioStefaniniCrudPedidos\.

6.3. - Escolha da Framework:

![Framework](/ImagensREADME/Net6.png "Framework.")


