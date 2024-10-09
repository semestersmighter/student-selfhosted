---
title: "1 : Wireguard Setup"
next: "2 : DNS Setup"
---

> WireGuard® is a VPN (Virtual Private Network) software designed for simplicity and efficiency. It is distinguished by its small codebase, which aims to reduce complexity and potential security 
> vulnerabilities, and offers faster performance compared to some other VPN solutions, due to its streamlined design.
![wireguard](https://www.wireguard.com/img/wireguard.svg)
[link to wireguard website](https://www.wireguard.com/)

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