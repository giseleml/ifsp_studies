# Paradigma RPC vs. Paradigma Orientado a Recursos:

### Paradigma RPC (Remote Procedure Call)
Cliente chamando um método dentro do programa que ele já sabe que existe, antes de usá-lo. 

- Exemplo: /calculadora (enviado os números a serem somados )

### Paradigma Orientado a Recursos 
Várias URL's que descentralizam a capacidade do sistema. 

- Exemplo: /calculadora/soma

# Path Parameters vs. Query Parameters:

### Path Parameters 
Paramêtros usados quando declaramos id's pros recursos, tendo uma ordem hierárquica. 

- Exemplo: /hoteis/1/quartos (listando os quartos que pertencem ao hotel 1, que pertence ao conjunto de todos os hotéis.)

### Query Parameters 
Usados quando queremos fazer uma consulta (query).
Podemos filtrar resultados oferecendo estes parâmetros, delimitados por um sinal de interrogação (?) e na sequência & e pares de <chave><valor>.

- Exemplo: /hoteis?cidade=saopaulo

Para incluir um segundo parâmetro, separamos com &:

- Exemplo: /hoteis?cidade=saopaulo&disponibilidadetipo=quartosuperior

### Body Parameter
Parâmetro que passamos no corpo da requisição. 

- GET suporta corpo apenas como resultado da requisição.
- POST, PUT e PATCH  suportam corpo tanto na requisição quanto na resposta.
- HEAD e OPTIONS não permitem corpo.

### HATEOAS (Hypermedia As The Engine Of Application State)
Técnica em que todo o estado de conversação entre cliente e servidor seja mantido pela própria hipermídia. 

- Hipermídia: conteúdo que tem referências para outras mídias. 

- Sem HATEOAS: /hoteis/<id do hotel>/quartos
- Com HATEOAS: Quebramos essa URL em duas /hoteis/id e /quartos, e referenciamos os quartos à partir dos hóteis. 