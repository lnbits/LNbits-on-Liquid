# LNbits on Liquid 🤯

Using trustless atomic swaps via boltz to run LNbits of Liquid!

Video tutorial using lunanode:

### Install LNbits

```
wget https://raw.githubusercontent.com/lnbits/lnbits/main/lnbits.sh &&
chmod +x lnbits.sh &&
./lnbits.sh
```

### Install Boltz
https://github.com/BoltzExchange/boltz-client/releases

```
tar -xvzf <release>
cd bin/linux
chmod +x boltzd
chmod +x boltzcli

# Run boltz and create a Liqud wallet
./boltzcli --standalone
./boltzcli wallet create lnbits lbtc
```

### Install Greenlight

https://blockstream.com/green/

### Set you DNS records

![image](https://github.com/user-attachments/assets/2ad63f5e-4f9a-4500-a4e4-b8f02ae321dc)

### Install and run caddy

https://caddyserver.com/docs/install#debian-ubuntu-raspbian

```
caddy reverse-proxy --from example.com --to :5000
```
