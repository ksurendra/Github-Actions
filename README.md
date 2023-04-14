# Github Actions
Example Workflows to run Github Actions.

## Google Cloud
### Google Cloud App Engine
1. `gcloud-app-helidon-java.yml` - Manual deploy a [Helidon Application](https://helidon.io) (uses Oracle Java 17) to Google App Engine.
  
   - Uses Google Cloud App Engine projet's Json Key. (Google Cloud console > IAM & Admin > Service Accounts > Select project's ellipsis > Manage Keys > Add Key > Create new keyt > Download the JSON)
   - Add this json as a Secret to Github repository (Repository > Settings > Secrets and variables > Secrets > Add Secret)

## Firebase
1. `firebase-hosting-manual-develop.yml` - Manual deploy code (Angular) to Firebase app.
2. `firebase-hosting-pull-request-develop.yml` - Auto deploy code (Angular) on a Pull Request on 'develop' branch. 
3. `firebase-hosting-pull-request-main.yml` - Auto deploy code (Angular) on a Pull Request to 'main' branch. 

   - For all the above, uses Firebase Service Account and Github Token.
   - Firebase has certain process to link Fiurebase account with Github. 
      
      - I used `$ firebase login:ci` that generates a Token, w=whihc can then be added to Github Repository as a secret.

## Digital Ocean
### Digital Ocean App
1. `digitalocean-app-nestjs.yml` - Manual deploy code (Nest JS Framework) branch to Digital Ocean App.
   
   - Uses DigitalOcean's Access Token for the App.

### Digital Ocean Droplet
1. `digitalocean-droplet-nestjs.yml` - Manual deploy code (Nest JS Framework) branch to Digital Ocean droplet.

   - Uses Digital Oceam droplets' Private Key, Remote Host and Remote User. 
   - Generate a private key on your computer. Uplaod that to DigitalOcena Droplet and to Github repository as a Secret (Repository > Settings > Secrets and variables > Secrets > Add Secret).