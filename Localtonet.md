LocalToNet
How to run proxy server using localtonet
download localtonet on ubuntu using terminal
then make it work, using authentication code provided on dashboard homepage


go to bench and do bench use SITENAME
like bench use 192.168.29.37 and hit enter

do bench use sitename , like bench use 192.168.29.79
afterwards, do bench start


do add domain under sites/yoursite/site_config.json
"domains": [
  "abhyudayunicorp.com"
 ]

now go to,
https://localtonet.com/tunnel/http
enter your local link like 192.168.29.37 and port whatsoever(in our case 80 because we would like to use production) and then its gone live! congrats it works!!!


to run tunneling from system to localtonet, run this is current folder

cd /home/abc/Desktop/Localtonet/localtonet-linux-x64/ && ./localtonet authtoken SECURE_KEY_BY_LOCALTONET

## Setup to autorun website using localtonet (CRON JOB
do crontab -e
then enter @restart cd /home/abc/Desktop/Localtonet/localtonet-linux-x64/ && ./localtonet authtoken SECURE_KEY_BY_LOCALTONET
and hit save, then restart, so from next time , you will see it autorunning on startup
