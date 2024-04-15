Sample commands

Interactive terminal:
`docker run -it ubuntu bash`
then:
`exit`

Run python terminal:
`docker run -it python:3.9`
exit python prompt:
Ctrl+d


## to execute the Dockerfile
`docker build -t test:pandas .`
then
`docker run -it test:pandas`

## setting up ny_taxi postgres db
```
docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v $(pwd)/ny_taxi_postgres_data:/var/lib/postgresql/data \
  -p 5432:5432 \
  postgres:16
```