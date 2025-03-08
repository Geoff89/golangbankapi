# golang Backend using Gin Framework, Postgres, and Deployment to AWS EKS Cluster.
This is a back end for a  bank api using Golang, AWS Kuberenetes and Postgres. Below are basic commands to start postgres database.
- docker run --name postgres12 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret -p 5432:5432 -d postgres:12-alpine
- docker exec -it postgres12 psql -U root
- docker logs postgres12


#### To create postgres database inside inside a container shell use below instructions
- docker exec -it postgres12 /bin/sh
- createdb --username=root --owner=root simple_bank
## To delete the database use the below command
- dropdb simple_bank

#### Create/drop database outside postgres container
- docker exec -it postgres12 createdb --username=root --owner=root simple_bank
- docker exec -it postgres12 psql -U root simple_bank

