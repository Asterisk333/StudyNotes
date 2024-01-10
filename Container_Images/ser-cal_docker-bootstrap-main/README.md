# Docker Einstieg

## Containerized App

Dieser Ordner beinhaltet sämtliche files um einen Container zu bauen, der eine einfache Web-App beinhaltet (express, handlebars...)

- Gitlab Registry Image: [ser-cal/docker-bootstrap:webserver_one](https://gitlab.com/ser-cal/docker-bootstrap/container_registry/3511633)


## Multi-Container

Dieser Ordner beinhaltet sämtliche files, um eine Multi-Container Web-App mit "docker-compose" zu erstellen
- Python Flask App mit Redis Cache
- Gitlab Registry Image: [ser-cal/docker-bootstrap:webserver_one](https://gitlab.com/ser-cal/docker-bootstrap/container_registry/3511633)

## Swarm Stack

Dieser Ordner beinhaltet sämtliche files, um eine Multi-Container Web-App mit einem Swarm Stack zu bauen.
- Eine einfache Python Flask App mit Redis Cache, welche zusätzlich den aktuellen Hostnamen (ID) des Containers auflistet, der den Request bearbeitet hat (Layer 3 Loadbalancing)
- Docker hub image: [ser-cal/docker-bootstrap:swarm-stack](https://gitlab.com/ser-cal/docker-bootstrap/container_registry/3516549)
