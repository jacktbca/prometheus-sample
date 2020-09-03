# Prometheus Sample

This repository simply run the Prometheus, Grafana, node-exporter to test the alert functionality of prometheus. But the notification from alertmanager still needs to be set up in alertmanager.yaml.



## Start 

after you git clone the repository, you could command docker-compose to run the sample.

```
$ docker-compose up -d
```

the ports of Prometheus, Grafana are 9090 and 3000 respectively. You could check the settings in the docker-compose.yml file.

- Open your browser to check [prometheus](http://localhost:9090)

  > you could check alert function in alert tab page

- Open your browser to check [Grafana](http://localhost:3000)

  > you need to setup the Grafana by some steps



### Settings 

the content of `alert.rules` file describes the alert criteria. You could change the alert description in details.



### Test

You could test the alert function by 

```
$ docker-compose stop node-exporter
```

Then you go to the alert tab page of prometheus on browser, you could check the alert is in pending state. And after a few minutes, the state will become Firing. Then the alert is shooting. You could set the alertmanager.yaml to notify what you want to notify.





