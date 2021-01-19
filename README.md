# Transactions_FacundoAcuna

This repository contains the definition for the operation of the application for technical test.
One part consists of an Angular 10 application that displays on the screen the list of transactions for
One account.
The other part consists of a Rest API application made with Net Core 3.0 where you can
find transaction operations for an account.
The API does not use persistence to a database but uses an in-memory database,
when executing the API an account and three transactions are loaded into memory
to have a sample of data.
There is also an API for operations with the accounts.



## Preparation and use
The API operations can be tested with Postman or another tool.
Here is how to use each of the available operations:

GET operation:
Retrieves the list of all available transactions
URL: https://localhost:44393/api/transactions

You can also retrieve an individual transaction sent the parameter by querystring
URL: https://localhost:44393/api/transactions/1



POST operation:
Create a new transaction for the account, the parameter must be a json in the body
of the request as shown below

  {
    "id": 5,
    "amount": 600.00,
    "effectiveDate": "2021-01-19",
    "type": 1,
    "accountId": 1
  }

URL: https://localhost:44393/api/transactions


## Features
The API contains validations regarding the existence of accounts, duplication of operations
and use of transactions to control data changes.
Before testing the operations, note that in-memory databases they are not relationally supported
, that is, you should not delete an account that has assigned transactions.
