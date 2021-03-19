# Veramo Labs Context Definitions

Repository for various use cases used for demo purposes only.

## Example: DID Document

```json
{
   "@context":[
      "https://www.w3.org/ns/did/v1",
      "https://identity.foundation/EcdsaSecp256k1RecoverySignature2020/lds-ecdsa-secp256k1-recovery2020-0.0.jsonld"
   ],
   "@id":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798",
   "verificationMethod":[
      {
         "@id":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798#controller",
         "@type":"EcdsaSecp256k1RecoveryMethod2020",
         "controller":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798",
         "blockchainAccountId":"0xb9c5714089478a327f09197987f16f9e5d936e8a@eip155:1"
      },
      {
         "@id":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798#controllerKey",
         "@type":"EcdsaSecp256k1VerificationKey2019",
         "controller":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798",
         "publicKeyHex":"0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798"
      }
   ],
   "authentication":[
      "did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798",
      "did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798#controllerKey"
   ]
}
```

## Example: ID Verification provider issues KYC VC to creator of NFT

```json
{
   "@context":[
      "https://www.w3.org/2018/credentials/v1",
      "https://veramo.io/contexts/kyc/v1"
   ],
   "@type":[
      "VerifiableCredential",
      "VerifiableKyc"
   ],
   "@id":"https://idcheck.com/433423223",
   "issuer":{
      "@id":"did:web:idcheck.com"
   },
   "issuanceDate":"2010-01-01T19:23:24Z",
   "credentialSubject":{
      "@id":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798",
      "@type":"Person",
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
      "https://veramo.io/contexts/nft/v1"
   ],
   "@type":[
      "VerifiableCredential",
      "VerifiableNft"
   ],
   "issuer":{
      "@id":"did:ethr:0x0279be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798"
   },
   "issuanceDate":"2010-01-01T19:23:24Z",
   "credentialSubject":{
      "@type":"Nft",
      "@id":"did:nft:<cryptopunk-#1>",
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
      "https://veramo.io/contexts/socialmedia/v1",
      "https://schema.org"
   ],
   "@type":[
      "VerifiableCredential",
      "VerifableSocialMediaPosting"
   ],
   "@id":"https://dtwitter.com/tweets/1234",
   "issuer":{
      "@id":"did:nft:<crypto-punk-#1>"
   },
   "issuanceDate":"2010-01-01T19:23:24Z",
   "credentialSubject":{
      "@type":"SocialMediaPosting",
      "author":{
         "@id":"did:nft:<crypto-punk-#1>",
         "type":"Person",
         "image":"https://ipfs.io/ipfs/QmT4AeWE9Q9EaoyLJiqaZuYQ8mJeq4ZBncjjFH9dQ9uDVA",
         "name":"cryptopunk"
      },
      "headline":"punks are aliens",
      "articleBody":"waffles for zoomers"
   },
   "credentialSchema":{
      "id":"https://veramo.io/contexts/socialmedia/v1/eip712",
      "type":"Eip712SchemaValidator2021"
   },
   "proof":{
      
   }
}
 ```
