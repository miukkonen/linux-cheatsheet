# Linux cheatsheet


### Make a tar -package
 	tar -cvzf package.tar.gz filename

### Unzip tar package
	tar -zxvf package.tar.gz

### What distro and version do I have?
	cat /etc/*-release

### What kernel do I have?
	dpkg --list | grep linux-image

### Check the drive information
	sudo parted -l

or

	df -h

or maybe the best option:

	sudo fdisk -l

### RAM situation
	free -mth

Note! "Free" means memory that is empty, "available" means something that has cache and buffers, but could be used when needed.

### What is my IP to the outside world?
	curl -s ipinfo.io/ip
or
	curl ident.me
	
### Changing the hostname

	sudo vim /etc/hostname
	sudo vim /etc/hosts

Change the hostname in these files and reboot



Palomuuriasetukset

	iptables -L


Näytä suurimmat tiedostot/hakemistot

	sudo du -hs * | sort -rh | head -5


Lokitiedostojen tyhjentäminen turvallisesti

	sudo su
	cd /var/log
	> ufw.log
	> kern.log
	> syslog

	(mennään roottina kirjoittamaan tiedostot tyhjiksi. Ei saa tehdä rm -käskyllä! Tiedostojen pitää olla koko ajan olemassa ja muiden prosessien saatavilla)


Sähköpostin lähetys komentoriviltä

	echo "Tämä on asiani" > note.txt
	echo "Subject: Asiaa" | cat - note.txt | sendmail -F Pacius mikko.oikkonen@intrin.fi









