# Serviço de Restaurante

## Endpoints

### Crud

- Endpoint para incluir um novo Restaurante
- Endpoint para Atualizar um Restaurante
- Endpoint para Deletar um Restaurante
- Endpoint para consultar um Restaurante por id
- Endpoint para consultar lista de restaurantes
- Endpoint para cadatrar um novo Prato
- Endpoint de Solicitação de Pedido

### Regras

#### Incluir um novo Restaurante

- Todo documento deve ser salvo no banco de maneira criptografada

#### Endpoint para Deletar um Restaurante

- Garantir que se uma consulta estiver sendo realizada no mesmo momento do cancelamento que já não exiba o restaurante que esta sendo atualizado.

#### Endpoint para cadatrar um novo Prato

- Um Restaurante só pode ter somente 100 pratos

### Enpoint de solicitação de pedido

- Esse endpoint receberá os dados de um pedido com id do pedido, informações do prato
- O restaurante tem o limite de 10 refeições no máximo para cada prato, ou seja se o cliente solicitou o 11º de um prato no dia o restaurante irá retornar para o sistema de pedidos o status "CANCELADO_RESTAURANTE"
- Se o pedido estiver dentro do limite o restaurente irá chamar o endpoint de atualização de status passando o status  "PREPARANDO_RESTAURANTE"
