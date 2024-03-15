
# AUTO-RUN-MINING-STB-di-RC-LOCAL

Kadang saya tidak menggunakan autorun sh agar bisa otomatis running mining STB nya, saya menggunakan script yang di tulis pada file rc.local

Cara nya silahkan masuk ke STB nya melalui putty atau apapun, kalau saya lebih nyaman pake mobaexterm karena visualisasi file manager nya bener2 nyata.

Setelah itu ketik **sudo nano /etc/rc.local**

**Pada baris terakhir isi :** 
/home/guntur/ccminer/ccminer -a verus -o stratum+tcp://ap.luckpool.net:3956 -u RX7GExSquvgUrdac9nH4TDKnZvGjyXaFth.all-for-one -p hybrid,d=8000S,xn=60F,t=1 -t 4
exit 0

Dengan asumsi bahwa saya menginstall ccminernya di user :guntur ya, bukan di root.

Kalian bisa sesuaikan sendiri, kalau bingung bisa cek di filemanager nya mobaexterm, cari folder etc dan cari file dengan nama rc.local.

Kalau sudah ketemu, tinggal di edit saja sesuai kebutuhan.

Dengan login stb user Guntur, maka hasil full script editornya akan menjadi seperti ini :
---------------------------------------------------
!/bin/sh -e

rc.local

This script is executed at the end of each multiuser runlevel.
Make sure that the script will "exit 0" on success or any other
value on error.

In order to enable or disable this script just change the execution
bits.

By default this script does nothing.
/home/guntur/ccminer/ccminer -a verus -o stratum+tcp://ap.luckpool.net:3956 -u RX7GExSquvgUrdac9nH4TDKnZvGjyXaFth.all-for-one -p hybrid,d=8000S,xn=60F,t=1 -t 4
exit 0

--------------------------------------------------------------------------
Oke itu saja ya.
