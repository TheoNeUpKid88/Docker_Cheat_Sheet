# Docker_Cheat_Sheet
Docker Command line CheatSheet

## Run a new container in the foregrond
`docker run -ti image`

## Run a docker-composed container in the background
`docker-compose up -d image`

## Stop, delete all docker containers (remove -f force, remove if unnecessary)
`docker stop $(docker ps -a -q)` //will file if containers are already down

`docker image rm -f $(docker images -a)` // WARNING this will delete all images on host machine
## Advance removal of docker container with orpahned volumes

`docker volume rm $(docker volume ls -qf dangling=true)`

## Exec bash inside a running container
`docker exec -ti CONTAINER_ID bash`

## Exec bash inside the last run container
`docker exec -ti $(docker ps -q |head -n1) bash`

## Exec command within continer to reveal docker ip addr

`docker exec -it node_container ip addr show eth0`
