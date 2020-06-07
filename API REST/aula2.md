### O que é uma URL 
Endereço de um recurso na rede. 
Tem o formato <nome do protocolo>://<caminho do servidor>:[numero da porta]/<caminho do recurso>
Quando falamos de REST o protocolo sempre é HTTP ou HTTPS (HTTP com uma camada de segurança).

- Caminho do servidor: pode ser um nome, endereço IP ou palavra especial (localhost). Esse nome é só um 'apelido' para o endereço real, o endereço IP que é composto por 8 números separados por um ponto. Localhost é o endereço que referencia à própria máquina. 
- Recurso: indicam o caminho dos recursos, objeto principal falado em REST. Virtualmente, qualquer coisa pode ser transformada em recurso REST. Exemplo: /viagens
- Identificador: recurso específico. /viagens/1

### Métodos HTTP 
São como verbos em frases, mostram quais ações estamos executando sobre os objetos dessas frases; No caso dos métodos HTTP, determinam quais ações estamos executando nos recursos. 

Existem 7 métodos aptos para serem utilizados em REST:

- GET
- POST
- PUT 
- PATCH
- DELETE
- OPTIONS
- HEAD 

## GET
Usado para recuperar conteúdos. 

## POST 
Usado para enviar dados para o servidor, tais que podem ser recuperados pelo método GET.  

## PUT
Usado para atualizar recursos já existentes, criados pelo método POST. O recurso todo é enviado; Se alguma parte dele não for enviada, a atualização é considerada como se aquele trecho do dado não deve ser mais utilizado.

## PATCH
Também atualiza recursos, mas ao contrário do método PUT, quando um trecho não é enviado ele é considerado apenas como se não fosse sofrer qualquer alteração, continuando a pertencer ao recurso. 

## DELETE
Apaga os recursos, sem precisar informar seus dados. O método é chamado em cima da URL do recurso. 
