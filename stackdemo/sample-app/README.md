# Set up a Docker registry

* Create a throwaway registry, which you can discard afterward( it will be used to store docker images for swarm cluster)
* $ docker service create --name registry --publish published=5000,target=5000 registry:2

### Check its status with

$ docker service ls

### Test the app with Compose

$ docker-compose up -d

### Bring the app down

$ docker-compose down --volumes

### Push the generated image to the registry

$ docker-compose push

## Deploy the stack to the swarm

$ docker stack deploy --compose-file docker-compose.yml stackdemo

### Check that it’s running with:

$ docker stack services stackdemo

## Bring the stack down with:

$ docker stack rm

### Bring the registry down with:

$ docker service rm registry
