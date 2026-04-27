## Server
### 1- Configure the server to listen on port `514/tcp` <br>
  `sudo firewall-cmd --permanent --add-service=syslog` <br>
  `sudo firewall-cmd --permanent --add-port=514/tcp`
  
### 2- Restart the firewalld service <br>
  `sudo firewall-cmd --reload`
  
  <img width="494" height="416" alt="listenport-server" src="https://github.com/user-attachments/assets/b19eb68b-7a1e-4c5c-b9c2-e1d1909186eb" />



### 3- Customize the `rsyslog` service to receive and save the remote logs under the specified path
  - Open the `/etc/rsyslog.conf` and uncomment the following line:
      - input(type="imtcp" port="514")
  - Add the configuration in the `/server` directory in this repo 

### 4- Restart the `rsyslog` service <br>
  `sudo systemctl restart rsyslog.service`
---

## Client
### 1- Configure the `rsyslog` as well
  - Add the configuration in the `/client` directory in this repo

### 2- Restart the `rsyslog` service
  - `sudo systemctl restart rsyslog.service`
