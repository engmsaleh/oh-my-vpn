# oh-my-vpn!
Setup your own OpenVPN server in 30 seconds! and secure your naked internet connections before it is too late.

### Server Setup
Pick a new cheap server, CPU and Memory does not really matter
The following one-liner script installs Chef and related depedencies and provision openvpn-server and generates the client configuration file.

### Use the one-liner script (Server):
```
curl -L http://git.io/pdTu | sh
```
A generated file for openvpn-client should exist at ```/root/client.conf```

### Post-Installation (Client):

- Install OpenVPN on your machine.
- Copy the client-config and place it under your OpenVPN client configuration directory  ```/etc/openvpn```
- Restart openvpn service on your laptop ``` service openvpn restart```

If you are using GUI OpenVPN client, you can just read the generated configuration file and replicate the config to your GUI client, ```It is readable by humans```. Also you will find the SSL certificates embded into the file. 

### Supported Operating Systems:

``` Ubuntu 14.10 ```
``` Ubuntu 13.10 ```

### TODO
- Email the client certificates to the user email
- Add recipe to configure the client machine
- Pipe-line the project to Travis-ci for continous testing
- Add Support Ubuntu [14.04, 13.04, 12.10, 12.04] and Debian [7.4, 7.0]
