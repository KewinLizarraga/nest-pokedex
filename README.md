<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

# Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar

```sh
yarn install
```

3. Tener Nest CLI instalado

```sh
npm i -g @nestjs/cli
```

4. Levantar la base de datos

```sh
docker-compose up -d
```

5. Clonar el archivo ***.env.template*** y renombrar a ***.env***

6. Llenar las variables de entorno definidas en el ***.env***

7. Ejecutar la aplicación en dev:

```sh
yarn start:dev
```


8. Reconstruir la DB con la semilla

```
http://localhost:3000/api/v2/seed
```

---

## Stack usado
* MongoDB
* NestJS

---

# Production Build

1. Crear el archivo ***.env.prod***
2. Llenar las variables de entorno de prod
3. Crea la nueva imagen

```sh
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```