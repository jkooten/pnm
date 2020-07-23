# pnm-ofdmarxmer-filedecode-v2
# dependencies with hexdump, GD::Graph and Data::Hexdump

A simple perl script that will turn your OfdmaRxMer PNM binary file ino a nice graph with correct(!) data.
 
Just feed the PNM file to the script and it wil decode the file for you conform CableLabs CM-SP-CCAP-OSSIv3.1-I17-191204 specification (table 410 in the spec to be more accurate)

There is some pretty printing when the script is kicked off.
Tested agains several CCAP devices (Arris E6000 REL8.0, Casa C100G rel 8.6.2 and Cisco cBR-8 rel ios-xr 16.12.1y/z)
There will be an update once Casa fixes the issue that there is no such thing as 2kHz subcarrier spacing. for Casa 50kHz spacing is assumed when other not correct values are found in the PNM file.

the PNM images will be stored in /var/ww/html/pnm but you can change that if you want offcourse.

# EXAMPLE (i changed the CMTS name and replaced the actual mac address for xxxxxxxxxxxx)

./pnm-ofdmarxmer-filedecode-v2 /tftpboot/PNMCcapRxMER_CCAP002_xxxxxxxxxxxx_1403405123

504e4e69 ==> OFDMARxMer
Date of PNM Measurememt ==> 2020-06-05 18:12:23
Interface Index = 34234577
Modem Mac Address = xxxxxxxxxxxx
Subcarrier 0 frequency = 11325000
FIRST ACTIVE SUBCARRIER = 74
Subcarrier spacing = 50000 Hz
Amount Active Subcarriers = 448
First Subcarrier Frequency = 15025000
Last Subcarrier Frequency = 37425000


# set-pnm-ofdmarxmer-meas

There is also a small script to help you do the snmpset commands to get the OfdmaRxMer PNM measurement started.
pretty straight forward. Just run it and it will do the snmpsets for you.

"./set-pnm-ofdmarxmer-meas <CCAP-NAME> <MODEM MAC> <IFINDEX> <SNMP RW COMMUNITY STRING>"

