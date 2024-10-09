---
title: "1 : Wireguard Setup"
next: "2 : DNS Setup"
---

# I - Installation 
```terminal
sudo apt update && apt upgrade -y
sudo apt install wireguard
```

# II - Generating public and private keys on the server

## II.1 - Create a directory to store the keys
```terminal
mkdir -p /etc/wireguard/keys
```

## II.2 - Create the public and private key
```terminal
cd /etc/wireguard/keys
umask 077
wg genkey | tee privatekey | wg pubkey > publickey
```