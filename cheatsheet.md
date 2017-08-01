# Linux cheatsheet


## Make a tar -package
 tar -cvzf package.tar.gz filename

## Unzip tar package
	tar -zxvf package.tar.gz

## What distro and version do I have?
cat /etc/\*-release

## What kernel do I have?
dpkg --list | grep linux-image

## Check the drive information
sudo parted -l
  or
df -h
  or maybe the best option:
sudo fdisk -l

## RAM situation
free -mth

Muisti

	free -mth

	(huom. "free" tarkoittaa muistia jossa ei ole mitään, "available" tarkoittaa muistia jossa on cachea ja buffereita, ja jossa siis on jotain, mutta joka voidaan tarvittaessa jyrätä)


Mikä on koneen ulospäin näkyvä ip-osoite? (intrinsicin verkon ulkopuolelle näkyvä)

	curl -s ipinfo.io/ip
		tai
	curl ident.me

