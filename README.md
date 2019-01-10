# Docker_Cheat_Sheet
Docker Command line CheatSheet

## Run a new container in the foregrond
`docker run -ti image`

## Stop, delete all docker containers (remove -f force, remove if unnecessary)
`docker stop $(docker ps -a -q)`

`docker image rm -f $(docker images -a)`

## Exec bash inside a running container
`docker exec -ti CONTAINER_ID bash`

## Exec bash inside the last run container
`docker exec -ti $(docker ps -q |head -n1) bash`

## Exec command within continer to reveal docker ip addr

`docker exec -it node_container ip addr show eth0`
