### Before You Begin
1. The server has access to the internet for downloading the Prometheus binary.
2. Most importantly, firewall rules opened for accessing Prometheus port 9090 on the server.

###  How To Install and Configure Prometheus On a Linux Server
Step1:Run the following commands are one by one on a linux server
```sh
cd /opt/
```
```sh
sudo wget https://github.com/prometheus/prometheus/releases/download/v2.29.2/prometheus-2.29.2.linux-amd64.tar.gz
```
```sh
sudo tar xf prometheus-2.29.2.linux-amd64.tar.gz
```
```sh
sudo rm -rf prometheus-2.29.2.linux-amd64.tar.gz
```
```sh
sudo mv prometheus-2.29.2.linux-amd64/ prometheus
```
Step2:
1. Update the target ips with port number on prometheus.yml file.For that,run the following commands are one by one on a linux server
2. Make sure that present working directory is /opt/ if not cd into it
```sh
cd /prometheus/
```
```sh
sudo vi prometheus.yml
```
## Note:
1. Update the targets under static_configs in prometheus.yml.For example
2. privateip is the ip of linux server where nodeexporter is installed and 9100 is port number of nodeexporter
```sh
global:
  scrape_interval: 10s

scrape_configs:
  - job_name: 'prometheus'
    scrape_interval: 5s
    static_configs:
      - targets: ['localhost:9090','priavteip:9100']
```
Finally,call the prometheus script using below command
```sh
sudo  ./prometheus
```
### Access Prometheus Web UI
Now you will be able to access the prometheus UI on 9090 port of the prometheus server.
```sh
http://<prometheus-ip>:9090
```








