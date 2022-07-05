# Serviço de Cliente

## Endpoints

### Crud

- Endpoint para incluir um novo Cliente
- Endpoint para Atualizar um Cliente
- Endpoint para Deletar um cliente
- Endpoint para consultar um Cliente por id
- Endpoint para cadatrar um novo endereço
- Endpoint para remover endereço


### Regras

#### Incluir um novo Cliente 

- Nesse serviço você deverá garantir que armazenará informações como : Nome completo do cliente, email, celular, documento ( CPF ).
- O sistema não aceitará novos clientes sem o nome, documento, email.
- Não será permitido cadastrar mais de um cliente com mesmo documento ou email.
- Será necessário validar o formato do documento .
- Será necessário validar o formato do E-mail.
- Registrar data de criação completa no cadastro

#### Atualizar um Cliente

- É possível atualizar algum campo do cadastro , como nome, telefone e email. Por exemplo se eu desejar atualizar meu nome no cadastro eu só enviarei esse campo.
- Caso a pessoa atualize o telefone ou o e-mail é necessário validar o formato
- Validar na atualização de e-mail se o e-mail já consta na Base de dados.
- Registrar a data completa de atualização no cadastro

#### Endpoint para Deletar um cliente

- Permitir a exclusão recebendo o e-mail do cliente.
- Deletar TODOS os dados do cliente

#### Endpoint para consultar um Cliente por id

- Consulta de cliente deve receber o id do cliente
- Deverá haver um parametro booleano que permitirá informar se deve retornar a lista de endereços do cliente também.

#### Endpoint para cadastrar um novo endereço

- O Endereço do cliente deve seguir o modelo completo com ponto de referência
- Um cliente pode ter vários endereços

#### Endpoint para remover endereço

- É possível remover um endereço realacionado a um cliente


