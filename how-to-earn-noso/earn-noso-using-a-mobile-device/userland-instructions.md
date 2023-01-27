# Userland instructions:

{% hint style="warning" %}
These instructions  only work if  you are using Userland
{% endhint %}

```
Go on play store and install Userland. Once installed, install Debian from inside Userland. Set username and password (some versions dont require this), and SSH (terminal) connection type (installation can take a while on old hardware). 

Then once logged into Debian perform the following steps:

sudo apt-get update --allow-releaseinfo-change

sudo apt-get update -y

sudo apt-get upgrade -y

sudo apt-get install wget -y

sudo apt-get install nano -y

sudo wget https://nosocoin.com/docs/download/consominer2-v1.6-arm32-linux

sudo chmod +x consominer2-v1.6-arm32-linux

./consominer2-v1.6-arm32-linux

ALT+X
CTRL+C

sudo nano consominer2.cfg
(set your wallet address, CPU to 6 (if 8 core) 3 (if 4 core), and test to false here)

CTRL+X (and when prompted type Y to save changes)

./consominer2-v1.6-arm32-linux
```
