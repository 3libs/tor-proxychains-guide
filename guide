## Install Tor
```
sudo apt install tor -y
```

## Test Tor
```
sudo systemctl start tor
sudo systemctl stop tor
```

## Edit the Proxychains config file
```
sudo nano /etc/proxychains.conf
```

    Remove ‘#’ from Dynamic chain
    comment ‘#’ Strict chain and Random chain
    Remove ‘#’ from proxy DNS
    write socks5 127.0.0.1 9050 in last line of proxy list


## Start Tor again and test the dynamic proxychain
```
sudo systemctl start tor
proxychains firefox www.google.com
```

After running the above commands firefox will launch and www.google.com will load.
Also please close all firefox tabs before executing the commands. 
Now you are using proxy chains!

To verify, go to an IP address detecting website like https://www.dnsleaktest.com/
If the IP and/or country changed, you are using the proxychain.
