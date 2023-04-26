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

### The development workflow (which only works on WSL so far)

1. Run `swa` using:

```bash
swa start
```
## Setting environment variable for db connections string

### For Windows (powershell)

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

$env:DATABASE_CONNECTION_STRING=''

$env:DATABASE_CONNECTION_STRING
```

### For Unix

```bash
export DATABASE_CONNECTION_STRING=''

export | grep DATABASE_CONNECTION_STRING
```
