# pnm
Docsis 3.1 PNM measurements. Mainly OFDM Downstream RX MER and OFDMA Upstream RX MER.

I was struggeling in the lab to get this 3.1 PNM visual. We did not have a good tool in lab environment to make it visible. 
Yes you can do a hexdump of the PNM file and put it in excel.....but i thought...let me just try to script it so that i can ust run the script, feed the PNM file to the script and an output image will be shown.
everything in perl for now. planning to rework this to python but no hurry on my side since the need is fullfilled :).


I am working on Usptream Triggered Spectrum Capture but implementation on CCAP/CMTS is not that sophisticated and output is bit more complex (and time is lacking).
Cable Modem Downstream Histogram PNM decode is also ready but needs some more work. i can share this on request. 

Plans for future:
* rewright the code to python for all you devops guys out there ;)
* build influxdb and import all pnm data.
* schedule regular polling intervals for PNM.
* graphing in grafana
* PMA like analytics based on the data.

But....time is always a thing when you also have a filltime day job :)

if you have certain questions or needs please feel free to contact me.
Also if you need some help coping with 4G/5G interference in your network...i can help in more then 1 way
