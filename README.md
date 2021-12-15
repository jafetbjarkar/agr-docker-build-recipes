# AGR Docker Build Recipes
Collection of different Docker builds for AGR development.


## Some docker commands
`docker ps`
`docker kill ...`
`docker build . -t db:local` - db:local is the image property from compose file


## Update images
docker pull agrinventory/databases-sqlserver
docker pull agrinventory/databases-sqlserver-atvr
docker pull agrinventory/api:develop

