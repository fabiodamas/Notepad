# Notepad
Tips for dont forget


*** Docker and postgres:

docker network create --driver bridge postgres-network

docker run --name teste-postgres --network=postgres-network -e "POSTGRES_PASSWORD=123456" -p 5432:5432 -v /home/fabio/Desenvolvimento/PostgreSQL:/var/lib/postgresql/data -d postgres

docker run --name teste-pgadmin --network=postgres-network -p 15432:80 -e "PGADMIN_DEFAULT_EMAIL=fabio.damas@gmail.com" -e "PGADMIN_DEFAULT_PASSWORD=123456" -d dpage/pgadmin4

Acessar: http://localhost:15432 

Configurar:
host: teste-postgres
port: 5432
username: postgres
senha: 123456
