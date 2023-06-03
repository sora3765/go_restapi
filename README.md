# practice project

# create module
go mod init go_restapi
# start db
docker compose up -d
# remove db
docker compose rm -s -f -v
# start app
GO_ENV=dev go run .
# run migrate
GO_ENV=dev go run migrate/migrate.go