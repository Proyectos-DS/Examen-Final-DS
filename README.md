Declaro que esta entrega fue realizada de forma individual, sin asistencia externa, sin herramientas de generación automática, y cumpliendo con todas las reglas del examen.


**Estructura del proyecto**

```text
├── docker-compose.yml
├── initdb  [error opening dir]
├── kubernetes
│   ├── configmap.yaml
│   ├── legacy-app-deployment.yaml
│   ├── new-microservice-deployment.yaml
│   ├── secret.yaml
│   └── statefulset.yaml
├── legacy-app
│   ├── Dockerfile
│   └── requirements.txt
├── logs
│   └── historial-terminal.logs
├── new-microservice
│   ├── Dockerfile
│   └── requirements.txt
└── README.md
```


Creo las imágenes a partir de los Dockerfiles

```sh
$ cd legacy-app
$ docker build -t legacy-app:latest .
```

```sh
$ cd ../new-microservice/
$ docker build -t new-microservice:latest .
```

Estando en la raíz del proyecto: Levantar los servicios con Docker-Compose

```sh
$ docker-compose up
```