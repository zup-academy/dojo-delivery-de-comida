# Serviço de Pedido

## Endpoints

- Endpoint para incluir um novo Pedido
- Endpoint para Cancelar um Pedido
- Endpoint para consultar um Pedido
- Endpoint para atualizar status do Pedido
- Endpoint para listar pedidos por cliente
- Endpoint para listar pedidos por Restaurante

### Regras

#### Endpoint para incluir um novo Pedido

- O pedido tem que conter o cliente, restaurante, listas de pratos/itens, observação
- Um pedido possui uma lista de pratos/itens, essa lista contém por item identificador do prato, valor unitário do prato e quantidade.
- Na experiência do cliente é exibido a lista de endereços do cliente, através disso ele seleciona qual endereço será feita a entrega do pedido, este dado deve ser salvo no pedido.
- O mesmo cliente não poderá solicitar pedidos em sequência por menos de 5 minutos.
- O pedido deve ter registrado o total 
- Tipo de pagamento será somente em dinheiro 
- O retorno do endpoint deverá trazer todas as informações do pedido.
- Ao incluir um pedido o status dele será PENDENTE APROVAÇÃO RESTAURANTE

#### Endpoint para Cancelar um Pedido

- Os pedidos cancelados, tem o status alterado para CANCELADO
- Para cancelar um pedido será necessário apenas o id do pedido e do cliente
- Só será possível cancelar um pedido que esteja com status PENDENTE APROVAÇÃO RESTAURANTE
- O cliente que cancelar mais do que 10 pedidos no mês pagará uma taxa adicional nas suas compras do mesmo mês de 15% adicionais.

#### Endpoint para consultar um Pedido

- Permite consultar os dados completos do Pedido pelo Id
- É possível ter um parâmetro para escolher exibir os itens
- É possível ter um parêmtro para escolher exibir o endereço completo

#### Endpoint para atualizar status do Pedido

- Tipos de Status em ordem de execução: PENDENTE, APROVADO, CANCELADO, FAZENDO, FEITO, TRANSPORTE, ENTREGUE
- É necessário armazenar a data e hora de cada atualização para histórico futuros
- A atualização só é permitida para pedidos diferentes de Cancelado e Entregue.
- É necessário seguir a regra do fluxo de atualização, exemplo um pedido não pode mudar status de fazendo para entregue.

#### Endpoint para listar pedidos por cliente

- Listar apenas código do pedido, data do pedido, status e valor
- É possível filtrar por data ou status ou ambos

#### Endpoint para listar pedidos por Restaurante

- Listar apenas pedidos com status diferente de cancelado.
- Listar código do pedido, data do pedido, status e valor
- É possível filtrar por data ou status ou ambos
