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
## Remove ‘#’ from Dynamic chain and comment ‘#’ Strict chain and Random chain
<img width="645" height="364" alt="Screenshot 2025-09-24 202656" src="https://github.com/user-attachments/assets/d2084aad-f899-40c5-b4e2-df7c375c0f38" />

## Remove ‘#’ from proxy DNS
<img width="633" height="265" alt="Screenshot 2025-09-24 202725" src="https://github.com/user-attachments/assets/57302a66-770f-4e29-9b00-0b5e047c1ea7" />

## Write socks5 127.0.0.1 9050 in last line of proxy list
<img width="560" height="158" alt="Screenshot 2025-09-24 202736" src="https://github.com/user-attachments/assets/581663c8-1eed-4ff4-ba33-227c72e9d47e" />

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
