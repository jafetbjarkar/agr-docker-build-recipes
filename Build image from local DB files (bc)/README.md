# To build docker image from local db
1. Update agr-databases/docker-compose.override.yml
2. Build:
  `docker-compose -f docker-compose.override.yml build databases`
3. Deploy:
  `docker-compose -f docker-compose.override.yml up -d`
4. Trigger build: Open localhost:5100. See progress in docker container (see docker client)
  `curl 'http://localhost:5100'`
5. Wait
6. Now the prod and stg dbs should appear in the sqlserver container (port 1433)

## In a single command
docker-compose -f docker-compose.override.yml build databases && docker-compose -f docker-compose.override.yml up -d && curl 'http://localhost:5100'


# API connection strings
## appsettings.json
"AGRConnectionString": "Data Source=localhost,1433; Initial Catalog=6.3.0-test-prod; User=sa; Password=Strong!Password9; integrated security=true; Trusted_Connection=false",
"STGConnectionString": "Data Source=localhost,1433; Initial Catalog=6.3.0-test-stg; User=sa; Password=Strong!Password9; integrated security=true; Trusted_Connection=false"
    
## gulpfile.js
const developConnectionString = 'Data Source=localhost,1433;Initial Catalog=6.3.0-test-prod;User=sa;Password=Strong\!Password9;integrated security=true;Trusted_Connection=false';




