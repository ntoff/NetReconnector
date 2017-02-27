# NetReconnector
Script for Armbian 5.25 on a PCDuino3b/nano to take down the built in wifi adapter, unload the driver, reload the driver and bring back up the network in the event the network becomes unreachable.

```
cd ~
git clone https://github.com/ntoff/NetReconnector
cd NetReconnector
nano NetReconnector.sh 
```
Check the network card and ping target, then make it executable if it isn't already with

`chmod +x NetReconnector.sh`

Then edit the crontab with `crontab -e` and add this line which will run the script every 5 minutes.
```
*/5 * * * * ~/NetReconnector/NetReconnector.sh 
```
   
Log file will be generated as ~/wifisbroken.log

    
