# DockerFiles
to update docker hub image, just update the respected docker file and then run following commands:
### First build the image:
$ docker build -t [tag] [path of dockerfile]
### Then tag the image:
docker tag [ImageId] [username]/[doker-hub-repository]:[tag]

e.g: docker tag 34f3cd0048ee afzalmasood11/debian-bullseye-slim-ruby:2.3.8

### Push the image to DockerHub:
docker push <hub-user>/<repo-name>:<tag>

e.g: docker push afzalmasood11/debian-bullseye-slim-ruby:2.3.8