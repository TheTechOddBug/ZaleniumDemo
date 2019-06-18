# ZaleniumDemo

docker run -d --rm --network=test-network --name zalenium -p 4445:4444 -v /var/run/docker.sock:/var/run/docker.sock -v /home/ubuntu/selenium-server/volume:/tmp/node/home/seluser/data --privileged dosel/zalenium start --desiredContainers 1 --maxDockerSeleniumContainers 1

docker run -it --rm --network=container:zalenium --name maven-testing -v "$(pwd)":/usr/src -w /usr/src --privileged maven mvn clean test -Dos=linux -Dbrowser=chrome -Durl="https://www.google.com/" -Dnode="http://zalenium:4445"