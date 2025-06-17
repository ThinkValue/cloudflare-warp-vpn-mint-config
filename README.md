# Linux Mint: Cloudflare WARP Installation & Usage Guide

The official instructions can be found at: 
https://one.one.one.one/ 

## Installation

### 1. Add the Cloudflare GPG Key

```bash
curl -fsSL https://pkg.cloudflareclient.com/pubkey.gpg | sudo gpg --yes --dearmor --output /usr/share/keyrings/cloudflare-warp-archive-keyring.gpg
```

### Add this repo to your apt repositories
```bash
echo "deb [signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list
```
### YOU MAY NEED TO CHANGE THIS FILE: 
```bash
sudo nano /etc/apt/sources.list.d/cloudflare-client.list
```
TO: 
```bash
deb [arch=amd64 signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ noble main
````
At least untill Cloudflare release a supported version for the latest linux min release!

## Install
```bash
sudo apt-get update && sudo apt-get install cloudflare-warp
```
# USE
```bash
warp-cli registration new (run when first installing warp)
```
then 
```bash
warp-cli connect/disconnect
```
```bash
warp-cli status
```
For OPTIONS use:
```bash
warp-cli 
```
Then go to
https://www.speedtest.net/
to test if it's active.

![image](https://github.com/user-attachments/assets/6c2f5555-14c2-40a8-8fde-cab7013a53f6)
