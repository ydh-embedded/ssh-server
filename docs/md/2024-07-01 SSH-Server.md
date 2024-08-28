#ssh
#server
______________

# SSH-Server


```bash
	servermkfs.ext4 "/dev/disk/by-id/scsi-0Linode_Volume_VOL_11GB_"  
```
.



```bash
	mkdir "/mnt/VOL_11GB_"  
```
.

 
```bash
	mount "/dev/disk/by-id/scsi-0Linode_Volume_VOL_11GB_" "/mnt/VOL_11GB_"  
```
. 

  
```bash
	ssh [root@172.105.72.234](mailto:root@172.105.72.234)  
```
.

  
```bash
	apt install unattended-upgrades automatische Updates
```
.

  
```bash
	dpkg-reconfigure --priority=low unattended-upgrades automatische Updates Part 2
```
.

  
```bash
	adduser <Benutzer> <Benutzer>
	#Benutzername in neuen Benutzer wechseln
		
	#Passwort and enter
```
.


```bash
	usermod -aG sudo Benutzername Benutzer zum Superhelden Gruppe hinzufügen
```
.

  
```bash
	#Benutzer ausloggen und neu einloggen
```
.

  
```bash
	logout
	ssh cloud@1xx.1xx.1xx.1xx
```
.

_____________
### Authentification Key-Pair


```bash
	mkdir [F12]/.ssh Ordner für public Key erstellen
```
.  


```bash
	mkdir [F12]/.ssh && chmod 700 [F12]/.ssh Ordner für public Key erstellen mitadmin rechten  

```
.


```bash
	ssh-keygen -b 4096 public key erzeugen

```
.


```bash
	ssh-copy-id cloud@@1xx.1xx.1xx.1xx #puplic-key hochladen
```
.


```bash
	sudo nano /etc/ssh/sshd_config #Standard Port ändern ;)
```
.


```bash
	Port 22 in 2xx
```
.


```bash
	AddressFamily any in AddressFamily inet
```
.


```bash
	Permit root Login Yes in no
```
.


```bash
	PasswordAuthentification Yes in no
```
.


```bash
	sudo ss -tupln offene Ports anzeigen lassen
```
.


```bash
	sudo systemctl restart sshd
```
.

________________
### Firewall installieren

- 

```bash
	[WIN] + [R]
	ufw
```
.


```bash
	sudo apt install ufw
```
.
  

```bash
	sudo ufw status
```
.


```bash
	sudo ufw allow 2xx
```
.


```bash
	sudo ufw enable
```
.

____________________

### Website vorbereiten


```bash
	sudo apt-get install apache2
```
.


```bash
	sudo systemctl start apache2
```
.
  

```bash
	sudo nano /etc/ufw/before.rules Ping schlucken
```
.


```bash
	for Input
```
.


```bash
	#eine neue erste Zeile eingfügen
	-A ufw-before-input -p icmp --icmp-type echo-request -j DROP
```
.

  
```bash


```
.

_____________
### Installation Cloudron


```bash
	sudo su -
```
.


```bash
	wget [https://cloudron.io/cloudron-setup](https://cloudron.io/cloudron-setup)  
```
.


```bash
	chmod +x ./cloudron-setup  
```
.

```bash
	./cloudron-setup  
```
.


![bild]( .\C:\working-directory\SSH-Server\screen\lenode.png)
  

