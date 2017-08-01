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

	df -h

	sudo fdisk -l

### RAM situation
	free -mth

Note! "Free" means memory that is empty, "available" means something that has cache and buffers, but could be used when needed.

### What is my IP to the outside world?
	curl -s ipinfo.io/ip

	curl ident.me
	
