#Build an image

docker build -t postgres:9.3 .

#Run a container

docker run -p 5432:5432 -d --name db_postgres --restart=always postgres:9.3

#Connect to Postgres

psql -h localhost -p 5432 -U postgres -W

psql -h localhost -p 5432 -U pguser -W pgdb

#Connect to bash into container

docker exec -ti -u root db_postgres bash
