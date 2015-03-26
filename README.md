# oh-my-vpn!
Setup your own OpenVPN server in 30 seconds! and secure your naked internet connections before it is too late.

### Server Setup
Pick a new cheap server, CPU and Memory does not really matter
Install the required dependencies
Pull down the repository to your server
run chef-solo

### Install the dependencies first:

```
sudo aptitude update
sudo aptitude safe-upgrade -y -f
sudo aptitude install -y ruby ruby-dev build-essential wget git
sudo gem install ohai chef --no-rdoc --no-ri
```

### Pull-down the code and run chef-solo

```
cd /tmp/ && git clone https://github.com/alaa/oh-my-vpn.git
sudo chef-solo -c /tmp/oh-my-vpn/solo.rb
```

### Or just use the one-liner script:
```
curl -L http://git.io/pDWu | sh
```

### Post-Installation
After your run chef-solo, your OpenVPN server will be ready:
- Copy the generated config ```/root/client.conf``` and place it in your laptop at ```/etc/openvpn```
- Restart openvpn service on your laptop ``` service openvpn restart```

### Supporting Operating Systems

``` Ubuntu 14.10 ```
``` Ubuntu 13.10 ```
``` Debian 7.4 ```
``` Debian 7.6 ```

### TODO
- Email the client certificates to the user email
- Add recipe to configure the client machine
- Pipe-line the project to Travis-ci for continous testing
- Add Support RPM-based distros and ArchLinux
