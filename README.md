# Projeto Semana Partiunuvem

Aplicação utilizada durante a construção do nosso projeto na Semana Partiunuvem.
Aplicação TFTEC Cloud sendo executada em .Net Core e conectada a um banco SQL Server.

# Primeira Aula - Criando seu primeiro projeto em Cloud

![TFTEC Cloud](https://github.com/raphasi/partiunuvem/blob/master/EstruturaApp_IaaS.png "Semana Partikunuvem")


## Passos para você realizar o deploy da sua aplicação:
1 - Download ASP.Net Core 7

https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-7.0.5-windows-hosting-bundle-installer

2 - Após instalar seu servidor Windows Server 2022, execute o comando abaixo para realizar a instalação do IIS:


```cmd
   Install-WindowsFeature -name Web-Server -IncludeManagementTools

```
3 - Faça download da pasta do projeto utilizando o seguinte link:


   [https://github.com/raphasi/semanapartiunuvem/archive/refs/heads/master.zip](https://github.com/raphasi/partiunuvem/archive/refs/heads/master.zip)

4 - Copie a pasta "partiunuvem" para dentro do diretório c:\inetpub\wwwroot:
```cmd
  C:\inetpub\wwwroot\partiunuvem 
  
```
5 - Para os demais passos da configuração você deve acompanhar a Aula 02.


# Segunda Aula - Modernizando sua aplicação com Cloud


## Etapa de Modernização do Banco de dados
1 - Donwload e instalação do Net .Framework 4.8 na VM-DB:

https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net48-offline-installer

2 - Download e instalaçao do DMA (Data Migration Assistant) na VM-DB:

https://www.microsoft.com/en-us/download/confirmation.aspx?id=53595

3 - Demais etapas detalhadas na Live:
- Criar um uma instância de Server SQL para hospedar o Azure SQL Database
- Criar uma instância de Azure SQL Database
- Utilizar o DMA para rodar um Assessment de compatilbilidade do banco antes da migração
- Parar a aplicação (iisreset /stop)
- Utilizar o DMA para rodar a migração do Schema do banco
- Utilizar o DMA para rodar a migração dos dados para o Azure SQL Database
- Conferir os dados migrados
- Desabilitar o serviço do SQL no servidor de oriem (IaaS)
- Alterar o endereço na string de conexão do servidor de aplicação
- Desligar a VM-DB

## Etapa de Modernização da Aplicação
1 - Donwload e instalação do App Service migration assistant na VM-APP:

https://azure.microsoft.com/en-au/products/app-service/migration-tools/

2 - Demais etapas detalhadas na Live:
- Criar um App Service Plan
- Fazer Upgrade do App Service Plan para uma instância S2 (Somente quem estiver com conta trial)
- Criar um Projeto no Azure Migrate
- Utilizar o App Service migration assistant para migração do site
- Ajustar a string de conexão no seu Web APP
- Desligar a VM-APP


## Para todas as instruções referentes a como montar este ambiente, acompanhe as aulas do evento.

Aula01 - https://www.youtube.com/watch?v=MWdrCNYmDGw

Aula02 - https://www.youtube.com/watch?v=o0tqdyFVtGI

Aula03 - https://www.youtube.com/watch?v=GXe13QbW8wk

