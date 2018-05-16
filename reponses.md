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

##6.4.1

 * SHA1 : 5a11b9d391970a9be59d72f7e069b65c81f2118e

##6.4.2

 * docker image pull gradle:4.7.0-jdk8-alpine
 * gradle id : f438b7d58d0a
 * "Volumes": {"/home/gradle/.gradle":{}}

##6.4.3

 * docker volume create gradle-home
 * docker volume ls
 * DRIVER              VOLUME NAME
   * local               1ece63ff02886570185584d90e343f6ec6d06aa6a8baf1294df1a6a8dd83b858
   * local               1f87a41ca493236230e295a6f946df896e0f014d17d5863d6d2dd8c166e3f843
   * local               4d193a6a6d5f69fb98364fbea27a3147e9041dd6a404ca3a54d41bdc1f6eea90
   * local               d51c029d2b567abd5b8923d281b5bed361142b1d537e136bea3eec7cf1ca4990
   * local               gradle-home
   * local               nginx-logs

##6.4.4

 * docker container run --rm -ti -v $(pwd):/src -v gradle-home:/home/gradle/.gradle -w /src gradle:4.7.0-jdk8-alpine gradle build

##6.4.5

 * docker container run --rm -ti -v $(pwd):/src -v gradle-home:/home/gradle/.gradle -w /src -p 8001:8080 gradle:4.7.0-jdk8-alpine gradle bootRun
 * {"articles":[],"articlesCount":0}

