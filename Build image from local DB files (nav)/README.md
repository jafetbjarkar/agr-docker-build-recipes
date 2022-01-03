# To build docker image from local db
1. Create agr-databases/docker-compose.override.yml
2. Build:
`docker build . -t db:local`
3. Deploy:
`docker-compose -f docker-compose.override.yml up -d`
4. Trigger build: Open browser on localhost:5100. See progress in docker container (see docker client)
5. Wait
6. Now the prod and stg dbs should appear in the sqlserver container (port 1433)

## In a single command
`docker build . -t db:local && docker-compose -f docker-compose.override.yml up -d && curl 'http://localhost:5100'`

# API connection strings if connecting to local API build
## appsettings.json
"AGRConnectionString": "Data Source=localhost,1433; Initial Catalog=6.3.0-test-prod; User=sa; Password=Strong!Password9; integrated security=true; Trusted_Connection=false",
"STGConnectionString": "Data Source=localhost,1433; Initial Catalog=6.3.0-test-stg; User=sa; Password=Strong!Password9; integrated security=true; Trusted_Connection=false"
    
## gulpfile.js
const developConnectionString = 'Data Source=localhost,1433;Initial Catalog=6.3.0-test-prod;User=sa;Password=Strong\!Password9;integrated security=true;Trusted_Connection=false';

