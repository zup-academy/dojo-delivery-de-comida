# Serviço de Entrega

Esse serviço esta relacionado com a validação de pagamento através dos dados bancários do pedido.

## Endpoints

### Crud

- Endpoint para incluir um novo entregador
- Endpoint para Atualizar um entregador
- Endpoint para Deletar lógicamente um entregador
- Endpoint para consultar um entregador por id 
- Endpoint para consultar um entregador por email

### Regras

#### Incluir um novo Entregador

- Nesse serviço você deverá garantir que armazenará informações como : Nome completo, email, celular, documento ( CPF ), CNH.
- O sistema não aceitará novos entregadores sem o nome, documento, email.
- Não será permitido cadastrar mais de um entregador com mesmo documento ou email.
- Será necessário validar o formato do documento .
- Será necessário validar o formato do E-mail.
- Registrar data de criação completa no cadastro

#### Atualizar um Entregador

- É possível atualizar somente o telefone e nome. 
- Caso a pessoa atualize o telefone é necessário validar o formato
- Registrar a data completa de atualização no cadastro

#### Endpoint para Deletar lógicamente um Entregador

- Inativar os dados do entregador através desse endpoint
- Teremos os entregadores ativos e inativos

#### Endpoint para consultar um Entregador por id

- Consulta de cliente deve receber o id do entregador
- não será permitido consultar entregador inativo, somente ativo 

#### Endpoint para consultar um Entregador por email

- Consulta recebendo o email do entregador
- não será permitido consultar entregador inativo, somente ativo 



