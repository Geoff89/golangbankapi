# golangsimplebankapi
This is a back end for a simple bank api using Golang, AWS Kuberenetes and Postgres
#### docker run --name postgres12 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret -p 5432:5432 -d postgres:12-alpine
#### docker exec -it postgres12 psql -U root
#### docker logs postgres12
#### systemctl status postgresql
##### systemctl stop postgresql
#### systemctl start postgresql

createdb inside container shell
docker exec -it postgres12 /bin/sh
createdb --username=root --owner=root simple_bank
dropdb simple_bank

#### Create/drop database outside postgres container
docker exec -it postgres12 createdb --username=root --owner=root simple_bank

docker exec -it postgres12 psql -U root simple_bank

migrate create -ext sql -dir db/migration -seq add_sessions

go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
