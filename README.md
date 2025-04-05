device must be rooted for at / backup / restore commands

all pixel supported (tenser cpu's)

here is GOOGSETNV command : 
printf "AT+GOOGSETNV=\"CAL.Common.Imei\",0,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",1,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",2,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",3,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",4,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",5,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",6,\"31\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",7,\"50\"\r\nAT+GOOGSETNV=\"CAL.Common.Imei\",8,\"00\"\r\n" > /dev/umts_router & cat /dev/umts_router


fastboot oem set_config bootmode factory

echo 'AT+GOOGBACKUPNV\r' > /dev/umts_router & cat /dev/umts_router
echo 'AT+GOOGGETIMEISHA\r' > /dev/umts_router & cat /dev/umts_router

"copy the shown code"

echo -n pastehere > /mnt/vendor/persist/modem/cpsha

chmod 644 /mnt/vendor/persist/modem/cpsha
setprop vendor.sys.modem_reset 1


echo 'AT+GOOGBACKUPNV\r' > /dev/umts_router & cat /dev/umts_router
echo 'AT+Googverifyimeisha\r' > /dev/umts_router & cat /dev/umts_router



restore to normal bootmode>>>>

fastboot oem set_config bootmode normal



u can also fill the imei numbers and factory mode on devinfo.img 

![image](https://github.com/user-attachments/assets/336d03c4-e52b-46cd-a565-51d8f38d1e8d)
