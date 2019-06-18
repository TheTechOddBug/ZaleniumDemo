# ZaleniumDemo

docker run -d --rm --name zalenium -p 4445:4444 -v /var/run/docker.sock:/var/run/docker.sock -v /home/ubuntu/selenium-server/volume:/tmp/node/home/seluser/data --privileged dosel/zalenium start --desiredContainers 1 --maxDockerSeleniumContainers 1

