### features
* Run a Redis server locally in a Docker container
* Dockerized a Python web application written in Flask
* Built Docker images and pushed them to the Docker Hub registry
* Orchestrated multi-container applications with Docker Compose
* Replicated a production-like infrastructure anywhere
* Defined a continuous integration workflow using GitHub Actions


### Dokcer commands
* docker run -d --name redis-server redis
* docker ps
* docker ps -a
* docker network create page-tracker-network
* docker network ls
* docker network connect page-tracker-network redis-server
* docker run --rm -it \
             --name redis-client \
             --network page-tracker-network \
             redis redis-cli -h redis-server
* docker stop redis-server
* docker rm redis-server
* docker run -d --name redis-server -p 6379:6379 redis
* docker inspect redis-server
* docker build -t page-tracker .
* docker build -f Dockerfile.dev -t page-tracker .
* docker images
* docker build -t page-tracker:$(git rev-parse --short HEAD) .
* docker login -u realpython
* docker tag page-tracker:dde1dc9 realpython/page-tracker:dde1dc9
* docker push realpython/page-tracker:dde1dc9
* docker pull realpython/page-tracker
* docker volume create redis-volume
* docker run -d \
             -v redis-volume:/data \
             --network page-tracker-network \
             --name redis-service \
             redis:7.0.10-bullseye
* docker exec -it -u root page-tracker-web-service-1 /bin/bash
* docker compose up -d
* docker compose ps
* docker compose ps -a
* docker compose logs --follow
* docker compose stop
* docker compose restart
* docker compose down --volumes
* docker compose pause
* docker compose unpause
* docker compose --profile testing up -d
* docker compose logs test-service
* 