# DockerBasicAssignmentRepo
Docker Basic Assignment

There are 3 services:
1. **ProductServiceDockerDummy** - This is Spring boot API which access postgres database and uses Redis cache. Docker file is also present. To build the project simply **mvn clean package -DskipTests**. Once up it will automatically insert few dummy records in database related to products. 
2. **Redis Cache** - This is custom Redis cache docker image. It uses latest redis cache image available. It only consists of dockerfile. 
3. **Database Postgres** - This is custom Postgres database docker image. It uses latest Postgres database image available. It only consists of dockerfile.

**Step to Run**------------
1. Download the docker-compose.yaml file
2. Open cmd where the docker-compose.yaml file is downloaded.
3. start wsl and docker using '**wsl**' and '**docker**' commands if docker is not configured to start automatically
4. Run '**docker-compose up**'command to start all the services.
5. Access the curl endpoint with **http://localhost:8080/getAllProducts**

Once everything is up and running, we will get all the available products from database for first request and from cache for subsequent requests.
