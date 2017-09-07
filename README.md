docker-compose build
docker tag image_id momokeith/letsgo
docker push momokeith/letsgo
docker-machine env staging-containers
eval $(docker-machine env staging-containers)
docker ps
docker-compose -f production.yml up -d
