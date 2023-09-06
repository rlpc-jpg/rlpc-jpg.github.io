# inf

##### IP

LF: 192.168.210.1
LP: 192.168.210.22
WP: 192.168.210.33

#### how

###### LP:

```bash
sudo apt-get update
sudo apt-get install openssh-server
sudo apt-get ssh status
```

###### WP:

```powershell
ssh vmadmin@192.168.210.22
ssh-keygen
scp C:\Users\vmadmin\.ssh\id_rsa.pub vmadmin@192.162.210.22:~/.ssh
```

###### LP:

```bash
cat /home/vmadmin/.ssh/id_rsa.pub >> /home/vmadmin/.ssh/authorized_keys
```

###### WP:

```powershell
ssh -i C:\Users\vmadmin\.ssh\id_rsa vmadmin@192.162.210.22
```

###### LP:

1. /etc/ssh/sshd_config öffnen und nach PasswordAuthentication auf no setzten und # weg

2. ```bash
   sudo service ssh restart
   ```
