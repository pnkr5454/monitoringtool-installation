### Before You Begin
1. The server has access to the internet for downloading the Node-exporter binary.
2. Most importantly, firewall rules opened for accessing Node_exporter port 9100 on the server.

###  How To Install and Configure Node Exporter On a Linux Server
Step1: Run the following commands are one by one on a linux server
```sh
cd /opt/
```
```sh
sudo wget https://github.com/prometheus/node_exporter/releases/download/v1.2.2/node_exporter-1.2.2.linux-amd64.tar.gz
```
```sh
sudo tar xf node_exporter-1.2.2.linux-amd64.tar.gz
```
```sh
sudo rm -rf node_exporter-1.2.2.linux-amd64.tar.gz
```
```sh
sudo mv node_exporter-1.2.2.linux-amd64/ node_exporter
```
Step2: Start the node_exporter agent by using below commands
```sh
cd node_exporter
```
```sh
sudo ./node_exporter
```
Now Successfully running agent but we can also configure to run agent in background.
