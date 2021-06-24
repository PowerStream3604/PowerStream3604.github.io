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

### Data Hashing
The first step is to hash the message or the data. By inputting the message(data) through the hashing algorithm, it will return the hash value with same length.
The original message(data) could vary in length however the output's length will always be the same. This is one of the basic trait of a hashing algorithm.
For cryptocurrencies, message(data) is always hashed because dealing with fixed length strings makes the process smooth although it is not a must to hash the message(data) before signing.

### Signing
When signing the hashed message(data), PKC uses its private key to sign the data and its distinct public key to verify that you actually sent the message.
Although the notion of signing the message(data) with private key and verifying with its distinct public key is same for all PKC, but mathematical algorithm and mechanisms vary according to what digital signature algorithm you use.

### Verifying
With some mathematical operations this stage validates if the signature is actually signed by the private key of that distinct public key.
For instance, *A1* wrote a message to *B2*, hashed it and signed it using the private key. When *B2* receives the message, *B2* is able to verify by using the public key presented by *A1*.
*B2* can be certain that *A1* created the signature since *A1* is the only person having the private key that corresponds to that public key.

These 3 steps work altogether to ensure ***Integrity***, ***Autheticity***, ***Non-repudiation***.

**Integrity** can be ensured since the signature will totally differ if anything gets modified.

**Authenticity** can be ensured since only the holder of private key can create signature.

**Non-repudiation** can be ensured. Once the signature has been generated, ***A1*** can't deny having signed it in the future.(Unless his private key gets compromised)

### Digital signature in Blockchain(ethereum)
For instance, when you send/sign transactions, sign messages digital signature is used to validate if you are the owner of the account.

```python
print('Hello World!')
```
