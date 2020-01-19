# docker-mongodb-enterprise

docker build --build-arg MONGO_PACKAGE=mongodb-enterprise --build-arg MONGO_REPO=repo.mongodb.com -t $DOCKER_USERNAME/mongo-enterprise:$MONGODB_VERSION .

docker run --name mymongo -itd $DOCKER_USERNAME/mongo-enterprise:$MONGODB_VERSION

docker exec -it mymongo /usr/bin/mongo --eval "db.version()"

PS.Autobuild from github to dockerhub will cause file-not-found error while running this image, so it can only be pushed manually.
