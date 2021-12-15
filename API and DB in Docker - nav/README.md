## TO restore
### Stop and remove
docker stop agr_databases_1 agr_api_1 && docker rm agr_databases_1 agr_api_1
### Delete images
- henda images (docker client)
(or try the docker pull commands)
### Run docker compose
docker-compose -f docker-compose.override.yml up -d



## The docker compose file
* Name: docker-compose.override.yml



DB Images:
agrinventory/databases-sqlserver
agrinventory/databases-sqlserver-atvr
agrinventory/databases-sqlserver-bc:latest
