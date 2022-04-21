# ETH DevConnect Amsterdam 2022
## Tatum Workshop 22/04/2022

### Setup
In order to participate in the workshop, you need to sign up for Tatum API Key, which is used for communication with the platform and perform operations.

[Sign up here](https://dashboard.tatum.io)

### Part 1 - Postman collection for NFT minting

Postman collection for the workshop is available [here](./postman.json). You can import it to Postman and perform API calls for easy NFT minting.
Use you API Key obtained from your Dashboard profile.

``For US West region, use url https://api-us-west1.tatum.io.``

``For EU region, use url https://api-eu1.tatum.io.``

### Part 2 - set up your Tatum KMS

In order to setup your own Tatum KMS, follow [this guide](https://github.com/tatumio/tatum-kms).


For local docker setup, you can use following command:
```shell
### pull docker image
$ docker pull tatumio/tatum-kms

### store existing private key
$ docker run -it  -v $HOME/vol:/root/.tatumrc tatumio/tatum-kms storemanagedprivatekey MATIC --testnet
Enter private key to store:******************************************************************
Enter password to access wallet store:***** ### Any password you wanna use, will be remembered from the first usage
{
  "signatureId": "a6826cb1-b6ca-4c88-bf31-e63223a3b464"
}

###Daemon mode
$ docker run -it  -v $HOME/vol:/root/.tatumrc tatumio/tatum-kms daemon --api-key=YOUR_API_KEY --chain MATIC --testnet
```

### Part 3 - MetaMask signing
Guide available [here](https://docs.tatum.io/tutorials/how-to-use-tatum-and-metamask).

Example of simple HTML integration of minting NFT and signing with MetaMask can be found [here](./metamask.html)

For any questions, reach out on our [Discord channel](https://discord.gg/tatum).

Created by Tatum@2022.
