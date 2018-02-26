# FORNIX
Shell script to install an [Fornix Masternode](http://www.fornix.co/) on a Linux server running Ubuntu 16.04. Use it on your own risk.

***
## Installation:
```
wget -q https://raw.githubusercontent.com/zoldur/Fornix/master/fornix_install.sh  
bash fornix_install.sh  
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the Fornix Coin Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **10000** **Fornix** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Tools -> "Open Masternode Configuration File"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again.
10. Click **Start All**
11. If you are not able to see your **Masternode**, try to close and open your desktop wallet.

***

## Usage:

```
fornix-cli mnsync status
fornix-cli getinfo
fornix-cli masternode status
```

Also, if you want to check/start/stop **Fornix** , run one of the following commands as **root**:

```
systemctl status Fornix #To check the service is running.
systemctl start Fornix #To start Fornix service.
systemctl stop Fornix #To stop Fornix service.
systemctl is-enabled Fornix #To check whetether Fornix service is enabled on boot or not.
```

***

## Donations:  

Any donation is highly appreciated.  

**Fornix**: FCKnUddniRmYkZJgbMRFr8cv4j1AF8Ei3R  
**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf
