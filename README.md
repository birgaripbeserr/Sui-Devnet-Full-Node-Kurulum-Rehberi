# Sui-Devnet-Full-Node-Kurulum-Rehberi

İlgili adımları takip ederek aşama aşama node kurabilirsiniz arkadaşlar. Projenin Discord hesabına katılıp, rol almayı unutmayın lütfen. Discord hesaplarının linkini makalede yazdım. Kolay Gelsin.

Gereksinimler (minimum)
```
2 CPU
8 RAM
50 SSD
```
Node kurduktan sonra sonda söyleyeceğim işlemleri yapmayı unutmayın!!

Bir screen oluşturalım:
```
screen -S sui
```

Full nodeumuzu yükleyelim (15-20 dakika kadar sürebilir)
```
wget -O sui.sh https://raw.githubusercontent.com/kj89/testnet_manuals/main/sui/sui.sh && chmod +x sui.sh && ./sui.sh
```

Logları kontrol:
```
docker logs -f sui-fullnode-1 --tail 50
```

Daha sonra discorda giriyoruz ve mesaj atıyoruz #node-ip-application kanalına:https://discord.gg/UGAcZh6E

Not: #pick-a-role role kanalından da rol alabilirsiniz isterseniz emojilere tıklayarak.

Nodeunuzu kontrol etmek için: https://node.sui.zvalid.com/

## Yararlı Komutlar 

Loglar: 
```
docker logs -f sui-fullnode-1 --tail 50
```

Node silmek için:
```
sudo systemctl stop suid
sudo systemctl disable suid
sudo rm -rf ~/sui /var/sui/
sudo rm /etc/systemd/system/suid.service
```

Node durumunu kontrol:
```
service suid status
```

Node reset atma:
```
sudo systemctl restart suid
```

Node durdurma: 
```
sudo systemctl stop suid
```

Hepsi bu kadardı. Tebrikler node kurmuş oldunuz... :)
