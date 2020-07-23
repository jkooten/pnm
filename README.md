# pnm-ofdmarxmer-filedecode-v2

dependencies with :<br>
hexdump<br>
GD::Graph<br>
Data::Hexdump<br>

A simple perl script that will turn your OfdmaRxMer PNM binary file ino a nice graph with correct(!) data.<br>
 
Just feed the PNM file to the script and it wil decode the file for you conform CableLabs CM-SP-CCAP-OSSIv3.1-I17-191204 specification (table 410 in the spec to be more accurate)<br>

There is some pretty printing when the script is kicked off.<br>
Tested agains several CCAP devices (Arris E6000 REL8.0, Casa C100G rel 8.6.2 and Cisco cBR-8 rel ios-xr 16.12.1y/z)<br>
There will be an update once Casa fixes the issue that there is no such thing as 2kHz subcarrier spacing. for Casa 50kHz spacing is assumed when other not correct values are found in the PNM file.<br>

the PNM images will be stored in /var/ww/html/pnm but you can change that if you want offcourse.<br>

<b>EXAMPLE (i changed the CMTS name and replaced the actual mac address for xxxxxxxxxxxx)<br></b>

./pnm-ofdmarxmer-filedecode-v2 /tftpboot/PNMCcapRxMER_CCAP002_xxxxxxxxxxxx_1403405123<br>
<br>
504e4e69 ==> OFDMARxMer<br>
Date of PNM Measurememt ==> 2020-06-05 18:12:23<br>
Interface Index = 34234577<br>
Modem Mac Address = xxxxxxxxxxxx<br>
Subcarrier 0 frequency = 11325000<br>
FIRST ACTIVE SUBCARRIER = 74<br>
Subcarrier spacing = 50000 Hz<br>
Amount Active Subcarriers = 448<br>
First Subcarrier Frequency = 15025000<br>
Last Subcarrier Frequency = 37425000<br>
<br>
<br>
# set-pnm-ofdmarxmer-meas<br>
<br>
There is also a small script to help you do the snmpset commands to get the OfdmaRxMer PNM measurement started.<br>
pretty straight forward. Just run it and it will do the snmpsets for you.<br>
<br>
"./set-pnm-ofdmarxmer-meas <CCAP-NAME> <MODEM MAC> <IFINDEX> <SNMP RW COMMUNITY STRING>"<br>

