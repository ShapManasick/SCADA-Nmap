# SCADA Nmap Techniques

## Nmap Scripting Engine
* https://github.com/digitalbond/Redpoint/blob/master/BACnet-discover-enumerate.nse
* https://github.com/digitalbond/Redpoint/blob/master/codesys-v2-discover.nse
* https://github.com/digitalbond/Redpoint/blob/master/enip-enumerate.nse
* https://github.com/nmap/nmap/blob/master/scripts/fox-info.nse
* https://github.com/digitalbond/Redpoint/blob/master/modicon-info.nse
* https://github.com/digitalbond/Redpoint/blob/master/omronudp-info.nse
* https://github.com/digitalbond/Redpoint/blob/master/pcworx-info.nse
* https://github.com/digitalbond/Redpoint/blob/master/proconos-info.nse
* https://github.com/digitalbond/Redpoint/blob/master/s7-enumerate.nse
* https://github.com/digitalbond/Redpoint

## Tools
* arp-scan
* netdiscover
* GRASSMARLIN
* Nipper Studio
* BACnet

## Danger of Port Scanning
* There is a possibility that the scan will crash system.
* Never use the default scans, especially the following : -O -A
* Use Connect scans only (-T in nmap).
* Use the nmap -T2 settings.
* Do not scan UDP (-sU).
* Use -sV selectively.

## Low Risk Scans
* nmap -n -PR -sn
* nmap -n -sn
* nmap -n -sn -scan-delay 0.1 -top-ports 100
* nmap -n -sT -scan-delat 0.1 -p (selected port range)

## Medium Risk Scans
* nmap -n -sT --max-parallelism 1 -p (selected port range)
* nmap -n -sT --max-parallelism 1 -p-
* nmap -n -sT --max-parallelism 1 -p- -sV

## Medium Risk Scans
* nmap -n -sT -p- -A
* nmap -n -sT -sU -p- -A
* Any illegal flag combination scans (FIN/NULL/XMAS)

