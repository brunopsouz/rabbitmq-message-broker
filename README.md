# RabbitMQ Message Broker

Este projeto demonstra o uso do RabbitMQ para implementar um simples sistema de mensageria assíncrona com produtor e consumidor escritos em C#.
O produtor envia mensagens contendo um timestamp e um GUID para uma fila chamada `message`. O consumidor recebe essas mensagens de forma assíncrona, processa e confirma o recebimento (ack), garantindo a persistência e confiabilidade no tráfego de mensagens.

## Funcionalidades
- Criação de fila durável (`durable: true`)
- Publicação de mensagens persistentes
- Consumo assíncrono com confirmação manual (`BasicAck`)
- Exemplo didático para filas e mensageria distribuída

## Setup de Ambiente 
Antes de rodar os projetos, certifique-se de ter os seguintes requisitos instalados:
- Docker
- .NET 8.0

## Como Executar
- Clone o projeto:
```bash
https://github.com/brunopsouz/rabbitmq-message-broker.git
```
- Abra menu Manage NuGet Packages e certifique-se que o RabbitMQ esteja instalado:
```bash
dotnet add package RabbitMQ.Client
```
- Execute o Docker:
```bash
docker-compose up -d
```
- Certifique-se que ambos projetos estejam configurados como Startup Projects
```bash
botão direito na solution > Configure Startup Project > Multiple startup projects > Ambos com Action: Start
```
- Execute o projeto:
```bash
dotnet run
```
Acesse seu localhost pelo Docker e utilize usuário padrão guest.


-
