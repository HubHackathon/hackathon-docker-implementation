# hackathon-docker-implementation
Docker implementation for participants to easily access data sets.

## Prerequisites:

Docker Desktop:

https://download.docker.com/mac/stable/Docker.dmg (Mac)  
https://download.docker.com/win/stable/Docker%20Desktop%20Installer.exe (Win)

## Build image and container
* From base directory run:
`docker-compose up --build -d`

* Follow server logs: (note: container name will be changing)
`docker logs -f hackathon-docker-implementation_db_1`

## Tear down container
* From base directory run:
`docker-compose down`

## Contributing
### Adding a new datasource
Create a table create migration to configure a new table for your new data source, for example: 

https://github.com/HubHackathon/hackathon-docker-implementation/blob/master/config/002_create_glacier_melt.sql

Create a sql insert data migration to insert data into the newly created table, for example: 

https://github.com/HubHackathon/hackathon-docker-implementation/blob/master/config/003_insert_glacier_melt.sql
