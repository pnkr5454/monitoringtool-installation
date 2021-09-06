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







