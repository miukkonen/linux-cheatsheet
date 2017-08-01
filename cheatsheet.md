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

### Palomuuriasetukset

	iptables -L


### Largest files taking up the most disk space

	sudo du -hs * | sort -rh | head -5

### Safe way to empty log files in Ubuntu
	sudo su
	cd /var/log
	> ufw.log
	> kern.log
	> syslog

Writes the files empty. Don't remove with rm! The files should be readable and writable with other processes.

### Sending email on the command line
	echo "This is my story." > note.txt
	echo "Subject: Story" | cat - note.txt | sendmail -F Sender-name mikko.oikkonen@bitway.fi


### Add a user
	adduser pumpeli

### Adding user to a group
	adduser pumpeli git


### Scheduled tasks (CRON)

Shows tasks:

	crontab -l

Shows tasks of root user:
	
	sudo crontab -l

Edit my tasks:
	
	crontab -e

### The packages requiring system restart
	cat /var/run/reboot-required.pkgs

### Is my machine 32 or 64?
	grep --color=always -iw lm /proc/cpuinfo
	
If one of the flags is "lm" (long mode) the processor is 64 byte type

### Is my operating system 32 or 64?
	uname -a

It's possible to have 32-byte system on a 64-byte machine.

### What software packages do I have on my Ubuntu system?
	sudo apt list --installed

