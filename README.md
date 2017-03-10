# postgres-9.3-docker

#BUILD IMAGE
docker build -t postgres:9.3 .

#RUN CONTAINER
docker run -p 5432:5432 -d --name db_postgres --restart=always postgres:9.3

#CONNECT TO POSTGRES
psql -h localhost -p 5432 -U postgres -W
psql -h localhost -p 5432 -U pguser -W pgdb

#CONNECT TO BASH INTO CONTAINER
docker exec -ti -u root db_postgres bash
