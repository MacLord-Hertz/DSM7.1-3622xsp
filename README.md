# DSM7.1-3622xsp
vmware install

./rploader.sh update now
./rploader.sh fullupgrade now
./rploader.sh serialgen DS3622xs+
./rploader.sh satamap now

edit userconfig

"SataPortMap": "4"    "9"
"DiskIdxMap": "00"    "0"
"netif_num": "1",

./rploader.sh ext apollolake-7.1.0-42661 add https://raw.githubusercontent.com/pocopico/redpill-load/master/redpill-virtio/rpext-index.json

./rploader.sh ext apollolake-7.1.0-42661 add https://raw.githubusercontent.com/pocopico/redpill-load/develop/redpill-acpid/rpext-index.json

./rploader.sh build broadwellnk-7.1.0-42661

exec sudo reboot
