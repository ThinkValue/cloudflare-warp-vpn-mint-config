## INSTALL

# Add cloudflare gpg key
curl -fsSL https://pkg.cloudflareclient.com/pubkey.gpg | sudo gpg --yes --dearmor --output /usr/share/keyrings/cloudflare-warp-archive-keyring.gpg

# Add this repo to your apt repositories
echo "deb [signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list

#YOU MAY NEED TO CHANGE THIS FILE: /etc/apt/sources.list.d/cloudflare-client.list
TO: 
deb [arch=amd64 signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ noble main

At least untill Cloudflare release a supported version for the latest linux min release!

# Install
sudo apt-get update && sudo apt-get install cloudflare-warp

## USE

warp-cli registration new (run when first installing warp)

then 

warp-cli connect/disconnect

warp-cli status

warp-cli [for OPTIONS]
