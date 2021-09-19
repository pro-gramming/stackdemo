#### To check if the container is privileged or not :-

docker inspect --format='{{.HostConfig.Privileged}}' <container id>