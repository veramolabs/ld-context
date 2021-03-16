# Veramo Labs Context Definitions

Repository for various use cases used for demo purposes only.

## Example: ID Verification provider issues KYC VC to creator of NFT

```json
   {
      "@context":[
         "https://www.w3.org/2018/credentials/v1",
         "https://veramolabs.github.io/ld-context/contexts/kyc/v1"
      ],
      "type":[
         "VerifiableCredential",
         "VerifiableKyc"
      ],
      "id":"https://idcheck.com/433423223",
      "issuer":"did:web:idcheck.com",
      "issuanceDate":"2010-01-01T19:23:24Z",
      "credentialSubject":{
         "id":"did:ethr:0xabcd",
         "type":"Person",
         "name":"John Doe"
      },
      "proof":{
         
      }
   }
```

## Example: Creator of NFT issues NFT VC about NFC

```json
   {
      "@context":[
         "https://www.w3.org/2018/credentials/v1",
         "https://veramolabs.github.io/ld-context/contexts/nft/v1"
      ],
      "type":[
         "VerifiableCredential",
         "VerifiableNft"
      ],
      "issuer":"did:ethr:0xabcd",
      "issuanceDate":"2010-01-01T19:23:24Z",
      "credentialSubject":{
         "type":"Nft",
         "id":"did:nft:<cryptopunk-#1>",
         "numberOfTokens":1,
         "contractAddress":"0xeeeefffff",
         "contractType":"erc1155",
         "tokenId":"2322323",
         "chainId":1,
         "name":"Cryptopunk #1"
      },
      "proof":{
         
      }
   }
```

## Example: NFT issues Tweet VC

```json
   {
      "@context":[
         "https://www.w3.org/2018/credentials/v1",
         "https://veramolabs.github.io/ld-context/contexts/socialmedia/v1",
         "https://schema.org"
      ],
      "type":[
         "VerifiableCredential",
         "VerifableSocialMediaPosting"
      ],
      "id":"https://dtwitter.com/tweets/1234",
      "issuer":"did:nft:<crypto-punk-#1>",
      "issuanceDate":"2010-01-01T19:23:24Z",
      "credentialSubject":{
         "type":"SocialMediaPosting",
         "author":{
            "id":"did:nft:<crypto-punk-#1>",
            "type":"Person",
            "image":"https://ipfs.io/ipfs/QmT4AeWE9Q9EaoyLJiqaZuYQ8mJeq4ZBncjjFH9dQ9uDVA",
            "name":"cryptopunk"
         },
         "headline":"punks are aliens",
         "articleBody":"waffles for zoomers"
      },
      "credentialSchema":{
         "id":"https://veramolabs.github.io/ld-context/contexts/socialmedia/v1/eip712.json",
         "type":"Eip712SchemaValidator2021"
      },
      "proof":{
         
      }
   }
 ```
