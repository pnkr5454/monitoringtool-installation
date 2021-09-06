### Before You Begin
1. Most importantly, firewall rules opened for accessing grafana port 3000 on the server.
### 1. Create a grafana YUM repository using below command
```sh
sudo vi /etc/yum.repos.d/grafana.repo
```
### 2. Copy the below content to the above yum repository file and save it
For OSS releases:
```sh
[grafana]
name=grafana
baseurl=https://packages.grafana.com/oss/rpm
repo_gpgcheck=1
enabled=1
gpgcheck=1
gpgkey=https://packages.grafana.com/gpg.key
sslverify=1
sslcacert=/etc/pki/tls/certs/ca-bundle.crt
```
### 3. Install Grafana with the following commands:
```sh
sudo yum install grafana
```
### 4. Start the server with systemd:
To start the service:
```sh
sudo systemctl start grafana-server
```
and verify that the service has started:
```sh
sudo systemctl status grafana-server
```
Configure the Grafana server to start at boot:
```sh
sudo systemctl enable grafana-server
```
### Grafana Web UI
Now you will be able to access the Grafana Web UI on 3000 port of the grafana server.
```sh
http://<grafana-ip>:3000
```


