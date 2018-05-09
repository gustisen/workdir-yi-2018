# TP Realworld

##6.3.1

 * SHA 1 : commit 7a2e472d9d9e77ad7de8f4ace9e09d7597ee60f7

##6.3.2

 * https://github.com/mkenney/docker-npm/blob/master/node-8-debian/Dockerfile
 * le volume src/
 * docker image pull mkenney/npm:node-8-debian
 * id : 9af19a7f4e2c

##6.3.3 
 
 * docker container run --rm -i -v $(pwd):/src mkenney/npm:node-8-debian npm install
 
##6.3.4 

 * docker container run --rm -ti -v $(pwd):/src -p 8000:8080 mkenney/npm:node-8-debian npm run dev


