
# Install OpenVPN Access to Server on AWS EC2 Machine.

# Step:1 
Launch a t2 micro Ec2 instance in AWS. and in security groups enable TCP ports 943,443,22 and UDP 1194 for inbound rules and all traffic for outbound rules.

# Step:2 
Connect to machine through SSH

```sudo su```

```apt update```

```apt upgrade```

```apt update && apt -y install ca-certificates wget net-tools gnupg```

```wget -qO - https://as-repository.openvpn.net/as-repo-public.gpg | apt-key add -```

```echo "deb http://as-repository.openvpn.net/as/debian focal main">/etc/apt/sources.list.d/openvpn-as-repo.list```

```apt update && apt -y install openvpn-as```

# Step:3 
Now Check the status of OpenVpn service

```systemctl status openvpnas.service```

# Step:4 
Now configure openvpn using root permissions

```ovpn-init --force```  

Here select the configuration as default after executing the above query.

Here setup your password and confirm password.

After all the setup, Enter openvpn site with your AWS public IP followed by port 943 in chrome.

Ex:- https://server_ip:943/admin 

# OpenVPN network and user configurations

**1) Login with username and password(username: openvpn, password: as per the configuration)**

**2) Elaborate Configurations and select Network Settings, In Hostname or IP Address field enter server_public_IP or DNS name and save the settings.**

**3) Elaborate User Management and select user permissions. Here enter username, in more settings configure password and save the settings.**

**4) In User Management select user profiles, here download new profiles for users and send to users to give VPN Access.**


# OpenVPN client connect installation
 
**1) In order to connect to OpenVPN Access to Server, please follow these steps:**

**2) Download and install OpenVPN Connect App:**

For Windows OS : https://openvpn.net/client-connect-vpn-for-windows/

For Linux OS: https://community.openvpn.net/openvpn/wiki/OpenVPN3Linux

For Mac OS: https://openvpn.net/client-connect-vpn-for-mac-os/
 
**3) After downloading Launch OpenVPN Connect App.**

**4) After successfully launching select file and upload the file attached to this mail.**

**5) Here Click on connect and enter the password to start VPN and Here you can see the VPN status**

