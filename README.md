# ws-podman

Some example commands to use podman

## MS SQL Server

podman pull mcr.microsoft.com/mssql/server:2022-latest
podman run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<redacted>" -p 1433:1433 --name sql1 --hostname sql1 -d mcr.microsoft.com/mssql/server:2022-latest

