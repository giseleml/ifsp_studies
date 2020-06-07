### Negociação de Conteúdo
Qual será o formato dos dados a serem transferidos.

### Cabeçalhos HTTP que negociam tipo de dados
- Content-type
- Accept

Formato: Macro-tipo/Micro-tipo
- Exemplo: text/html
- */* (qualquer tipo de conteúdo)

### Códigos de Status
- Começam com 2: Sucesso
- Começam com 3: O resultado depende de outras requisições que ocorreram antes ou depois da atual
- Começam com 4: Falha ocorreu por erro do cliente
- Começam com 5: Falha ocorreu por erro do servidor

- Exemplo: 304 Not Modified - O resultado da requisição anterior ainda pode ser usado.

### Cachê sem depender de data
- Cálculo de Hash: sequência de caracteres que vão corresponder ao estado atual do recurso. Cabeçalho ETAG é preenchido por ele; Ele é mais útil na criação/atualização de um recurso. É comum usar o algoritmo MD5 para fazer este cálculo.
