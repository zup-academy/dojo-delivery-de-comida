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

- Nesse serviço você deverá garantir que armazenará informações como : Nome Fantasia, Razão Social, email, telefone, documento ( CPF ou CNPJ ), responsável, celular responsável, descrição, classificação( Doces, Salgados, Massas, Churrascaria, Hamburgueria, Outros), faixa de preço ( barato, médio e caro), endereço completo, horário de funcionamento.
- O sistema não aceitará novos Restaurantes sem o nome fantasia, documento, email e responsável.
- Não será permitido cadastrar mais de um restaurante com mesmo documento ou email.
- Será necessário validar o formato do documento .
- Será necessário validar o formato do E-mail.
- Registrar data de criação completa no cadastro.

#### Atualizar um Restaurante

- É possível atualizar nome fantasia, telefone , email, celular do responsável, descrição, classificação e faixa de preço.
- Caso a pessoa atualize o telefone ou o e-mail é necessário validar o formato
- Validar na atualização de e-mail se o e-mail já consta na Base de dados.
- Registrar a data completa de atualização no cadastro

#### Endpoint para Deletar um Restaurante

- Permitir a exclusão apenas lógica do Restaurante
- Deletar lógicamente TODOS os dados do Restaurante

#### Endpoint para consultar um Restaurante por id

- Consulta de Restaurante deve receber o id 
- Deverá haver um parametro booleano que permitirá informar se deve retornar a lista de pratos do Restaurante também.

#### Endpoint para consultar lista de restaurantes

- Permitir que seja possível buscar por : nome fantasia, classificação, faixa de preço, cidade, bairro.
- A busca deve retornar no máximo 40 elementos.
- Deve permitir trabalhar com paginação
- A lista deve retornar apenas, nome fantasia, endereço, descrição, classificação e faixa de preço.

#### Endpoint para cadatrar um novo Prato

- Um prato esta relacionado somente a um restaurante
- Um prato tem como informação, nome, valor, descricao

#### Endpoint de Solicitação de Pedido

- Este endpoin é utilizado para informar ao restaurante que um pedido foi solicitado.
- O Restaurante deve registrar no dominio 

