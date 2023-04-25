# Vue Basic

[Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) allows you to easily build [Vue.js](https://vuejs.org/) apps in minutes. Use this repo with the [Vue quickstart](https://docs.microsoft.com/azure/static-web-apps/getting-started?tabs=vue) to build and customize a new static site.

## Project setup

```bash
npm install
```

### Compiles and hot-reloads for development

```bash
npm run serve
```

### Compiles and minifies for production

```bash
npm run build
```

### Lints and fixes files

```bash
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

## Running with SWA

### The production workflow (which works)

1. First build the application using:

```bash
npm run build
```

2. Then, run `swa` using:

```bash
swa start ./dist --data-api-location swa-db-connections
```


```bash
$env:DATABASE_CONNECTION_STRING='Server=dcaas-db.postgres.database.azure.com;Database=postgres;Port=5432;User Id=pgadmin;Password=QumPg123;Ssl Mode=VerifyFull;'

$env:DATABASE_CONNECTION_STRING
```

```bash
swa start ./dist --data-api-location swa-db-connections --run "npm run build"

swa start ./public --data-api-location swa-db-connections --run "npm run serve"
swa start ./src --data-api-location swa-db-connections http://localhost:8080
swa start ./public --data-api-location swa-db-connections

swa start
swa start http://localhost:8080 --run "npm run serve"
swa start ./src http://localhost:8080
swa start ./src --data-api-location swa-db-connections http://localhost:8080
swa start ./src --data-api-location swa-db-connections http://localhost:8080 --run "npm run serve"
swa start http://localhost:4280 --api-devserver-url http://localhost:8080
```
