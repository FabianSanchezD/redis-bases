# Práctica Redis

## Levantar Redis

```
docker pull redis
docker run --name mi-redis -d -p 6379:6379 redis
docker ps
```

## Correr los ejercicios

Uno por uno en la consola:

```
docker exec -it mi-redis redis-cli
```

O todos de una vez desde el archivo (las líneas con `#` se ignoran):

```
grep -v '^#' comandos.redis | docker exec -i mi-redis redis-cli
```

Ojo: el archivo termina con `FLUSHDB`. Las capturas de RedisInsight hay que tomarlas antes de esa línea.

## RedisInsight

Add Redis Database, host `localhost`, puerto `6379`, sin usuario ni contraseña.

## Archivos

- `comandos.redis`: todos los comandos en el orden de la guía.
- `entregable.md`: cada ejercicio con su comando y la salida de `redis-cli`.
- `capturas/`: capturas de RedisInsight.
