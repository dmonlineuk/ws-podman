# ws-podman

Some example commands to use podman

## MS SQL Server

```bash
podman pull mcr.microsoft.com/mssql/server:2022-latest
podman run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<redacted>" -p 1433:1433 --name sql1 --hostname sql1 -d mcr.microsoft.com/mssql/server:2022-latest
```

## prefect server

We can obviously include some env vars with the -e flag:

* PREFECT_SERVER_API_AUTH_STRING="admin:password"

```bash
podman pull prefecthq/prefect:3-latest 
podman run -p 4200:4200 -d prefecthq/prefect:3-latest -- prefect server start --host 0.0.0.0
```

## postgres

```bash
podman pull postgres:latest
podman run -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=p4s5W0rd -p 5432:5432 postgres --host 0.0.0.0
```

