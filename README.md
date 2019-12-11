# docker-mongodb-enterprise

export MONGODB_VERSION=4.2
export DOCKER_USERNAME=<username>

docker build --build-arg MONGO_PACKAGE=mongodb-enterprise --build-arg MONGO_REPO=repo.mongodb.com -t $DOCKER_USERNAME/mongo-enterprise:$MONGODB_VERSION .

docker run -p 27017:27017 nomomax/mongodb-enterprise
