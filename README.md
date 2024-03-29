<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>


# Teslo API

1. Clonar proyecto e instalar dependencias
2. ```yarn install```
5. Clonar el archivo ```.env.template``` y renombrarlo a ```.env```
6. Cambiar las variables de entorno
7. Levantar la base de datos
```
docker-compose up -d
```

1. Levantar: 
2. ```yarn start:dev```

5. Ejecutar SEED 
```
http://localhost:3000/api/seed
```


## Docker Repo Name
[klerith/teslo-shop-cors:latest](https://hub.docker.com/repository/docker/klerith/teslo-shop-cors/general)

## Implementar Docker Buildx para multiplataforma (amd64, amd64/v2) 
```
docker buildx create --name mybuilder --bootstrap --use
```
## Production notes:

Ejecutar este comando cuando este en producción
```
docker compose -f docker-compose.prod.yml build
```

## Docker Build para subir dos plataformas en dockerhub  
```
docker buildx build --platform linux/amd64,linux/amd64/v2 -t gregoryreyesp/nest-app-tienda:1.0.1 --push .
```
