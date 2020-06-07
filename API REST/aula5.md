### Modelos de Segurança para REST

## Autenticação Basic: usuário:senha. Com o algoritmo Base64 fazemos a mistura deles. 
- Exemplo: senha alesaudate:123456. O próximo passo é codificar esse valor usando Base64, que pode ser feito online. 
Codificado esse valor ficaria assim: 
- YWXLC2FIZGF0ZTOXMJMONTY=
Agora usamos esse valor no cabeçalho que será passado para todos os serviços que precisem de autenticação. 

Para incluir uma camada extra de proteção usamos HTTPS. Uma camada de criptografia colocada na comunicação toda, e que é automaticamente incriptada/decriptada quando cliente e servidor passam informações um para o outro.

Todo processo é transparente para o cliente, já o servidor precisa ser configurado para realizar essa criptografia que funciona com certificados de segurança. 

- Authorization: Basic Base64(usuario:senha)

## Autenticação OAuth
Permite que dois ou mais sites compartilhem informações de um usuário sem envolver a senha dele

- Consumer Key
- Shared Secret/Consumer Secret
- Request Token
- Tela de autenticação
- Access Token e Token Secret (Podem ser revogados, não são equivalentes à senha do usuário)
- Escopo do que a aplicação de terceiros podem fazer; É limitada. 

## OAuth 2
No OAuth 1 só havia um fluxo de funcionamento, o que no 2 se tornou diversos fluxos diferentes.

- Authorization Code
- Implicint Grant
- Resource Owner Password Credentials
- Client Credentials
- JWT (JSON Web Token)
- Fluxo de Revogação de Tokens

O principal é o Authorization Code. Semelhante ao OAuth 1, porém lá os parâmetros eram criptografados pelo cliente, e aqui são criptografados pelo HTTPS.

Dessa forma HTTPS deixa de ser opcional como no OAuth 1 e se torna obrigatório no 2. 

# Melhorias do OAuth 2 em relação ao OAuth1: 
- Pode ser utilizado por dispositivos mobile
- Pode ser utilizado por dispositivos IoT



