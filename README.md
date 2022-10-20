# dummy-deploy
This is a simple project to test deployment with docker-compose through a Github action.

## Preparing informations

### Generate a ssh key pair.
Got some issues with RSA generated with default parameters. Had good result with ed25519 : 
```
ssh-keygen -t ed25519
```

### Retrieve server public keys
We have to retrieve server public keys with this command :
```
ssh-keyscan -H ssh.myserver.com
```

## Set Github secrets
- Put the client public ssh key into a docker secret named `CLIENT_PRIVATE_KEY`.
- Put the server private key into a secret named `SERVER_PUBLIC_KEY`.
