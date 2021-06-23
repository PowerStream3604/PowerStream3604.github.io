---
title: "Crypto wallet login for dapps and crypto services"
date: 2021-06-23 18:05:54 -0400
categories: Wallet Login EIP javascript-ethereum-provider
---
## Digital signature
Digital signature is a mathematical technique to validate the authenticity and integrity of a message.
In blockchain, almost every action uses digital signature and it is the most basic and fundamental mathematical 
techique that comprises the blockchain technology. 
*(This article is wrote under the assumption that readers have basic knowledge about hash and PKC)*

Typically, there are 3 steps in digital signature in crypto world. 

1. Data Hashing
2. Signing
3. Verifying

These 3 steps work altogether to ensure *Integrity*, *Autheticity*, *Non-repudiation*

### Data Hashing

For instance, when you send/sign transactions, sign messages digital signature is used to validate if you are the owner of the account.

```python
print('Hello World!')
```
