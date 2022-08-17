# Serviço de Notificação

Objetivo desse serviço é centralizar o envio de e-mails e notificações para os clientes

## Endpoints

- Endpoint para solicitar uma nova notificação.
- Endpoint para consultar uma lista de notificação por e-mail e / ou por origem.
- Endpoint para consultar uma notificação pelo código.

## Regras

#### Solicitar uma nova notificação 

- Este endpoint irá atuar como a inclusão de uma nova solicitação de notificação
- Quando uma nova solicitação é feita, é gerada uma notificação incluida no banco de dados com status NÃO PROCESSADA
- Cada notificação tem como informação, tipo da notificação se será EMAIL, SMS.
- Teremos o campo contato, se o tipo for e-mail, o contato estará com o endereço de e-mail a ser enviada a notificação
- A notificação também tem titulo do aviso, o corpo do aviso, horário de solicitação e horário de envio. 
- É necessário armazenar também na solicitação a origem, ou seja, qual sistema solicitou o envio.
- Deve retornar o código da solicitação para consulta posteriormente

#### Atualizar um Cliente

- É possível consultar uma lista de notificações, passando como parâmetro o endereço de e-mail ou a origem , ou passar os dois para filtrar a listagem.
- Precisa usar paginação com limite de 50 itens por cada listagem.

### Rotina de envio

- Nesse sistema existirá uma rotina que irá pegar a cada 5 minutos a lista de notificações NÃO PROCESSADAS, irá enviar as notificação e após cada loto enviado irá atualizar as notificações como PROCESSADAS.




