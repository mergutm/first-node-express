# Modo desarrollo 
Usa **nodemon** para escuchar "cambios" en el código y se recompila al detectar cualquier cambio.


```bash 
docker compose --profile dev up --build
```


```bash 
$ docker compose --profile dev up --build
[+] Building 5.2s (12/12) FINISHED                                                                                                                                                                                                  
 => [internal] load local bake definitions                                                                                                                                                                                     0.0s
 => => reading from stdin 515B                                                                                                                                                                                                 0.0s
 => [internal] load build definition from Dockerfile                                                                                                                                                                           0.0s
 => => transferring dockerfile: 411B                                                                                                                                                                                           0.0s
 => [internal] load metadata for docker.io/library/node:18-alpine                                                                                                                                                              4.9s
 => [internal] load .dockerignore                                                                                                                                                                                              0.0s
 => => transferring context: 66B                                                                                                                                                                                               0.0s
 => [1/5] FROM docker.io/library/node:18-alpine@sha256:8d6421d663b4c28fd3ebc498332f249011d118945588d0a35cb9bc4b8ca09d9e                                                                                                        0.0s
 => [internal] load build context                                                                                                                                                                                              0.0s
 => => transferring context: 34.02kB                                                                                                                                                                                           0.0s
 => CACHED [2/5] WORKDIR /usr/src/app                                                                                                                                                                                          0.0s
 => CACHED [3/5] COPY package*.json ./                                                                                                                                                                                         0.0s
 => CACHED [4/5] RUN npm install                                                                                                                                                                                               0.0s
 => [5/5] COPY . .                                                                                                                                                                                                             0.0s
 => exporting to image                                                                                                                                                                                                         0.0s
 => => exporting layers                                                                                                                                                                                                        0.0s
 => => writing image sha256:cd21f2a24753b949723380f3934d60ac628389178f54255ad5a5b7edcd4c22da                                                                                                                                   0.0s
 => => naming to docker.io/library/express-web-dev                                                                                                                                                                             0.0s
 => resolving provenance for metadata file                                                                                                                                                                                     0.0s
[+] Running 3/3
 ✔ express-web-dev             Built                                                                                                                                                                                           0.0s 
 ✔ Network express_default     Created                                                                                                                                                                                         0.1s 
 ✔ Container node_express_dev  Created                                                                                                                                                                                         0.2s 
Attaching to node_express_dev
node_express_dev  | 
node_express_dev  | > node-express-app@1.0.0 dev
node_express_dev  | > nodemon server.js
node_express_dev  | 
node_express_dev  | [nodemon] 3.1.10
node_express_dev  | [nodemon] to restart at any time, enter `rs`
node_express_dev  | [nodemon] watching path(s): *.*
node_express_dev  | [nodemon] watching extensions: js,mjs,cjs,json
node_express_dev  | [nodemon] starting `node server.js`
node_express_dev  | Servidor ejecutándose en http://localhost:3000
node_express_dev  | [nodemon] restarting due to changes...
node_express_dev  | [nodemon] starting `node server.js`
node_express_dev  | Servidor ejecutándose en http://localhost:3000
```

# Modo producción


```bash 
docker compose --profile prod up --build -d
```
Puede usarse el parámetro -d para su ejecución en segundo plano.


## Detener el contenedor usando perfil
```bash 
docker compose --profile prod  down 
```

