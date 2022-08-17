# Serviço de Cliente

## Endpoints

### Regras

#### Incluir um novo Cliente 

- Todo documento deve ser salvo no banco de maneira criptografada

#### Endpoint para cadastrar um novo endereço

- O cliente só poderá cadastrar no máximo 4 endereços

#### Endpoint cartão cliente

- O cliente poderá cadastrar até 3 cartões para pagamento
- Os dados sensíveis do cartão deverão ser registrados com criptografia
- Deverá receber numero, bandeira, cvv, vencimento, endereço de cobrança e nome do cartão

#### Endpoint de consulta de cartões 

- Deverá ser possível consultar a lista dos cartões do cliente pelo seu id, somente dados básicos do cartão como id, bandeira e os ultimos quatro numeros do cartão

#### Endpoint de consulta de cada cartões

- Receber o id do cartão e devolver todos os dados. 

