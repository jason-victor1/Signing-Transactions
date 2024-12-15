# Signing Transactions

## Public and Private Keys
Public and private keys are crucial for blockchain transactions. A private key is a randomly generated secret used to sign transactions. This is passed through the Elliptic Curve Digital Signature Algorithm (ECDSA) to produce the corresponding public key. The private key remains confidential while the public key is accessible for transaction verification.

The below shows a private key being passed through the Elliptic Curve Digital Signature Algorithm (ECDSA) to produce the corresponding public key.

![Screenshot of Public and Private Keys](https://github.com/jason-victor1/Signing-Transactions/blob/main/public_private_keys.png?raw=true)


### Generating a Public Key from a Private Key
The private key is shown as a long hexadecimal string. When passed through ECDSA, it generates the corresponding public key. This can be shared openly while keeping the private key secret to secure the transaction process.

## How Transaction Signing Happens
When signing a transaction on the blockchain, data is digitally signed using the private key. The private key combines with the transaction data to create a unique message signature through a hashing algorithm. This ensures that the private key cannot be derived from the message signature while maintaining transaction security and integrity.

The below shows the private key hashed with the message data to generate a message signature. 
![Screenshot of Signing a Transaction](https://raw.githubusercontent.com/jason-victor1/Signing-Transactions/874729899776c33d444cb2828f31eec623f82a54/Signing%20a%20transaction.png)

The below shows that anyone can verify the transaction's validity by comparing the message signature with the public key. This ensures the transaction is authorized by the private key owner without revealing the private key itself.

![Screenshot of Verification Process](https://github.com/jason-victor1/Signing-Transactions/blob/main/verification.png?raw=true)


## Importance of Hiding Private Keys
Every Metamask account has a private key accessible through Account Details > Show Private Key, protected by a password. Keeping your private key safe is crucial, as anyone with access can sign and perform transactions on your behalf. This could potentially compromise your assets.

Wallet addresses provided by Metamask are derived from your public key. The public key is hashed using the Ethereum Hashing Algorithm, and the last 20 bytes of this hash become the wallet address. This ensures the address is uniquely tied to your key pair.
