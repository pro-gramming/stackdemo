## This repo demonstrate how you can create containers having similar capabilities as privileged one.

* pull-image.yml :- Docker-compose file to pull no. of docker images on every docker host in swarm.
* image-prune.yml :- Docker-compose file to remove unused docker images on every docker host in swarm.

##### To deploy the stack use:

* docker stack deploy --compose-file image-prune.yml image-prune
* docker stack deploy --compose-file pull-image.yml pull-image
