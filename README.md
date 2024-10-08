# LNbits on Liquid 🤯

Using trustless atomic swaps via boltz to run LNbits on Liquid!

Video tutorial using lunanode:
https://www.youtube.com/watch?v=AbWBagSHBsM
(We use `screen` sessions in the video tutorial to run but for production systemctl would make more sense)

### Install Boltz
https://github.com/BoltzExchange/boltz-client/releases

```
wget <amd-release>
tar -xvzf <amd-release>
cd bin/linux_amd64
chmod +x boltzd
chmod +x boltzcli

# Run boltz and create a Liqud wallet
./boltzd --standalone
./boltzcli wallet create lnbits lbtc
```

### Install LNbits

```
wget https://raw.githubusercontent.com/lnbits/lnbits/main/lnbits.sh &&
chmod +x lnbits.sh &&
./lnbits.sh
# Once finished ctrl+c to shut down
# To run again
export PATH="/home/$USER/.local/bin:$PATH"
./lnbits.sh
```

### Install Greenlight

https://blockstream.com/green/

### Set your DNS records

![image](https://github.com/user-attachments/assets/2ad63f5e-4f9a-4500-a4e4-b8f02ae321dc)

### Install and run caddy

https://caddyserver.com/docs/install#debian-ubuntu-raspbian

```
# Note your DNS record may take a while to propogate, so if this fails wait a little while and try again.
caddy stop
sudo caddy reverse-proxy --from yoururl.com --to :5000
```
