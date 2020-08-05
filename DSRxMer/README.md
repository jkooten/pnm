# pnm-ofdmrxmer-filedecode-v1

dependencies with :<br>
hexdump<br>
GD::Graph<br>
Data::Hexdump<br>
<br>
A simple perl script that will turn your OfdmDSRxMer PNM binary file ino a nice graph with correct(!) data.<br>
<br>
Just feed the PNM file to the script and it wil decode the file for you conform CableLabs CM-SP-CM-OSSI3.1-I10 specification (table 68 in the spec to be more accurate)<br>
<br>
There is some pretty printing when the script is kicked off.<br>
Tested agains several CM devices (Arris TG3492  and Ubee UBC1318)<br>
Until I10 the Major and Minor Version were not specified in the PNM output. <br>
As from I11 they are but the addaptation of anything larger then I10 is going slow....so at 1 point in time this script will need a minor update<br>
<br>
the PNM images will be stored in /var/ww/html/pnm but you can change that if you want offcourse.<br>
<br>
EXAMPLE<br>
<br>
./pnm-ofdmrxmer-filedecode-v1 /tftpboot/pnm/PNMDSMer_e4574007c740_050820201530<br>
<br>
504e4d04 ==> OFDM DSRxMer<br>
Date of PNM Measurememt ==> 2020-08-05 15:31:34<br>
Downstream Channel Index = 33<br>
Modem MAC Address =  e4574007c740<br>
Subcarrier Zero Frequency = 1019600000<br>
First Active Subcarrier = 158<br>
Subcarrier Spacing = 50 kHz<br>
Size OFDM Block = 189 MHz<br>
startdata = 25<br>
enddata = 3805<br>
