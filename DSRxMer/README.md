pnm-ofdmrxmer-filedecode-v1

dependencies with :
hexdump
GD::Graph
Data::Hexdump

A simple perl script that will turn your OfdmDSRxMer PNM binary file ino a nice graph with correct(!) data.

Just feed the PNM file to the script and it wil decode the file for you conform CableLabs CM-SP-CM-OSSI3.1-I10 specification (table 68 in the spec to be more accurate)

There is some pretty printing when the script is kicked off.
Tested agains several CM devices (Arris TG3492  and Ubee UBC1318)
Until I10 the Major and Minor Version were not specified in the PNM output. 
As from I11 they are but the addaptation of anything larger then I10 is going slow....so at 1 point in time this script will need a minor update

the PNM images will be stored in /var/ww/html/pnm but you can change that if you want offcourse.

EXAMPLE

./pnm-ofdmrxmer-filedecode-v1 /tftpboot/pnm/PNMDSMer_e4574007c740_050820201530

504e4d04 ==> OFDM DSRxMer
Date of PNM Measurememt ==> 2020-08-05 15:31:34
Downstream Channel Index = 33
Modem MAC Address =  e4574007c740
Subcarrier Zero Frequency = 1019600000
First Active Subcarrier = 158
Subcarrier Spacing = 50 kHz
Size OFDM Block = 189 MHz
startdata = 25
enddata = 3805
