---
description: Learn how to operate a Noso Masternode headless on Linux
---

# Headless Node

Noso's Masternode is designed to be run on a normal consumer PC featuring an information rich GUI that makes it easy for operators of any technical skill level to participate in the network security and earning rewards for doing so.&#x20;

However, in a more industrial context it is also often desired to run a node headless to automate the deployment process. This tutorial will show you an efficient way to set up a **headless** Noso Masternode on Ubuntu 22.04.&#x20;

{% hint style="info" %}
This tutorial is only recommended for experienced users that know their way around the command line as all graphical units that make Noso Masternodes so accessible will not be available to the operator.&#x20;
{% endhint %}

#### **Prerequisites:**

* Ubuntu 22.04 (VPS) meeting the minimum hardware requirements
* 10500 Noso&#x20;
* IPv4 not used for another Noso Masternode

***

#### Getting started:

For this tutorial we expect a fresh VPS Ubuntu 22.04 setup.

1. Update your system

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
```

2. Install required libraries

```bash
# Install GTK-2
sudo apt-get install gtk2.0 -y

# Install openssl for automatic updates
sudo apt-get install libssl-dev -y

# Install virtual desktop
sudo apt install xvfb -y
```

3. Download and extract latest Noso Masternode. As of writing this tutorial the latest version is v0.4.2Ca5. Replace <\<USERNAME>> with your user name.

```bash
mkdir /home/<<USERNAME>>/noso_node
wget -O node.tgz $node_link
tar -xzf node.tgz
mv Noso /home/<<USERNAME>>/noso_node/
chmod +x /home/<<USERNAME>>/noso_node/Noso
```

4. Start the node and let it set up the project environment. This usually only takes a couple of seconds.

```bash
cd /home/<<USERNAME>>/noso_node
nohup xvfb-run -a /home/<<USERNAME>>/noso_node/Noso &
```

5. Close the node

```bash
killall Noso
```

6. Make necessary changes in NOSODATA/advopt.txt. These are the minimal required changes that need to be done. Make sure to familiarise yourself with the settings file and make additional adjustments if needed. Replace <\<COLLATERAL>> with your fund address holding at least 10500 Noso.

```bash
# Switch setting
cd /home/<<USERNAME>>/noso_node/NOSODATA

# Add collatera addresss
sed -i "s/MNFunds [^ ]*/MNFunds <<COLLATERAL>>/g" advopt.txt

# Set Auto IP to TRUE
sed -i 's/MNAutoIp [^ ]*/MNAutoIp True/g' advopt.txt

# Activate MN
sed -i 's/Autoserver [^ ]*/Autoserver True/g' advopt.txt

# Set Full Node to FALSE
sed -i 's/WO_FullNode [^ ]*/WO_FullNode False/g' advopt.txt

# Turn off GUI refresh
sed -i 's/NoGUI [^ ]*/NoGUI False/g' advopt.txt
```

7. Restart your Node

```bash
cd /home/<<USERNAME>>/noso_node
nohup xvfb-run -a /home/<<USERNAME>>/noso_node/Noso &
```

Congratulations - you are now running a headless Noso Masternode. The default port for your node is 8080. Make sure to open that port in your firewall settings.&#x20;
