
### 1. Create a grafana YUM repository using below command
```sh
sudo vi /etc/yum.repos.d/grafana.repo
```
### 2. Copy the below content to the above yum repository file and save it
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


