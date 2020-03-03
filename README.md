# hackathon-docker-implementation
Docker implementation for participants to easily access data sets.

## Prerequisites:

Docker Desktop:

https://download.docker.com/mac/stable/Docker.dmg (Mac)  
https://download.docker.com/win/stable/Docker%20Desktop%20Installer.exe (Win)

## Build image and container
* From base directory run:
`docker-compose up --build -d`

* Follow server logs:
`docker logs -f hackathon-docker-implementation_db_1`

* If using Windows virtualization might need to be enabled:
    * Documentation about needing to enable virtualization (https://docs.docker.com/docker-for-windows/troubleshoot/#virtualization-must-be-enabled)
    * Steps on how to enable virtualization (https://mashtips.com/enable-virtualization-windows-10/)

## Tear down container
* From base directory run:
`docker-compose down`

## Query Data
* Connect to the docker container:
  * First run `docker exec -it hackathon-docker-implementation_db_1 /bin/bash`
  * Once connected to the container run `mysql --host=localhost --port=13306 --user=user --password=password hack_climate_change_2020`
* User a DB visualization tool such as [MySQL Workbench](https://www.mysql.com/products/workbench/) or [DBeaver](https://dbeaver.io/download/)
