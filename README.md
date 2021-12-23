# elk-jenkins

Log Jenkins job in ELK stack using docker-compose
Step by step:

1. Build jenkins and nginx docker images in [jenkis-container](/jenkins-container) and [nginx-container](/nginx-container) folder <br>
```docker build -t [CONTAINER_NAME] .```
2. Create container using docker compose <br>
```Run docker-compose -f docker-compose-jenkins.yml up -d``` <br>
```Run docker-compose -f docker-compose-elk.yml up -d```
3. Create and run jenkins build
4. See the log in ```localhost:9200``` for elasticsearch and ```localhost:5601``` for kibana
