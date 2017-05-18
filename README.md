Create data container to store config so it isn't lost between jenkins container restarts:
`docker run --name jenkins-data idenitjenk echo "Jenkins Data Container"

Run and link the jenkins container:
`docker run -d --name jenkins -p 8080:8080 --volumes-from jenkins-data -v /var/run/docker.sock:/var/run/docker.sock identijenk`

