# Serviço de Pedido

## Endpoints

### Regras

#### Endpoint para incluir um novo Pedido

- Só será possível incluir no máximo 5 pedidos por dia por cliente. 
- Lista nova de status que deve ser sustituida : SOLICITADO, AGUARDANDO_RESTAURANTE, CANCELADO, CANCELADO_RESTAURANTE,  PREPARANDO_RESTAURANTE, AGUARDANDO_ENTREGA, EM_ENTREGA, CONCLUIDO
- quando um pedido for incluido na base de dados, deverá em seguida chamar o endpoint de Restaurante para encaminhar o pedido e atualizar após isso o pedido para status AGUARDANDO_RESTAURANTE, somente em caso de sucesso.

#### Endpoint para Cancelar um Pedido

- O cliente que cancelar mais do que 10 pedidos no mês pagará uma taxa adicional nas suas compras do mesmo mês de 15% adicionais.

#### Incluir um novo pedido

- Nesse endpoint deverá consultar o serviço de cliente para validar se ele existe
- Nesse endpoint deverá consultar o serviço de Restaurante para validar se ele existe
- Nesse endpoint deverá consultar o serviço de Restaurante/Pratos para validar se o prato existe
- Chamar o endpoint para incluir o pedido no restaurante
