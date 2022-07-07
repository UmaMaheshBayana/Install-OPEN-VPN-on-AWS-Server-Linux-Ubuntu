
# SETUP OPEN VPN IN AWS LINUX SERVER

Connect to the machine and update the properties

```sudo apt-get update```
```sudo apt-get upgrade```

Installing the package 'OpenVPN' will automatically pull in the required client bundle as well.

```apt update && apt -y install ca-certificates wget net-tools gnupg```
```wget -qO - https://as-repository.openvpn.net/as-repo-public.gpg | apt-key add -```

```echo "deb http://as-repository.openvpn.net/as/debian focal main">/etc/apt/sources.list.d/openvpn-as-repo.list```

```apt update && apt -y install openvpn-as```
 
# To configure openvpn server

```ovpn-init --force```

Note:by executing the above command, you can configure the IP address and setup password. Here IP address will be displayed, open the IP address in google and login with username and password. 
