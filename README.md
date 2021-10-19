# Banking-Application
Simple Spring boot application which provide REST service for money transfer using Gradle.

Implemented a simple REST service with some very basic functionality - to add and read an account.
It is a standard gradle project, running on Spring Boot. It uses Lombok.

Added functionality for a transfer of money between accounts. Transfers specified by providing:
accountFrom id
accountTo id
amount to transfer between accounts
The amount to transfer should always be a positive number. 

Prerequisite :
- Gradle
- JDK 1.8+
- Lombok
- Spring Tool Suite 4

This application is for demo only. It provides APIs for following 2 features
- Create account
- Retrieve Account Balance
- Create Transaction

Basic API Information :

POST : Create Account
------
http://localhost:18080/v1/accounts
{"accountId": "1122", "balance": 9000}
{"accountId": "2233", "balance": 5000}


POST : Create Transaction (TRANSFER)
------
http://localhost:18080/v1/transfer

{
  "accountFromId": 2233,
  "accountToId": 1122,
  "amount": 20
}


GET : Retrieve account balance
-----
http://localhost:18080/v1/accounts/2233
