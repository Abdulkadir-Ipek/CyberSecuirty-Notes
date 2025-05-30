#ag #network #topoloji #subnetting #arp #dhcp #firewall #router #switch
# Ağ Topolojileri

Ağ topolojisi, bir bilgisayar ağındaki cihazların fiziksel veya mantıksal olarak nasıl düzenlendiğini gösteren yapıdır.  
Temel ağ topolojileri:

- **Yıldız (Star)**
- **Halka (Ring)**
- **Ağaç (Tree)**
- **Mesh (Örgü)**

Her topolojinin avantaj ve dezavantajları vardır.


---

## Subnetting

Subnetting, IP adreslerini alt ağlara bölme işlemidir. Bu sayede:

- Ağ kaynakları verimli kullanılır.
- Güvenlik artırılır.

**Temel Kavramlar:**

- **IP Adresi:** Örn. `192.168.1.1`
- **Subnet Mask:** Örn. `255.255.255.0`
- **CIDR Notasyonu:** Örn. `192.168.1.0/24`
- **Network Adresi:** Alt ağın ilk adresi
- **Broadcast Adresi:** Alt ağın son adresi
- **Kullanılabilir IP'ler:** Cihazlara atanabilen aralıktaki IP’ler


| CIDR | Subnet Mask       | Host Sayısı |
|------|--------------------|-------------|
| /24  | 255.255.255.0      | 254         |
| /25  | 255.255.255.128    | 126         |
| /26  | 255.255.255.192    | 62          |
| /27  | 255.255.255.224    | 30          |
| /28  | 255.255.255.240    | 14          |
| /29  | 255.255.255.248    | 6           |

---

## ARP Protokolü

**ARP (Address Resolution Protocol)**, IP adresini MAC adresine çevirir.  
Yerel ağda (LAN) çalışır ve OSI modelinin **Veri Bağı (Data Link)** katmanında yer alır.

> Cihaz, iletişim kuracağı cihazın IP adresinden MAC adresini ARP ile bulur.

---

## DHCP Protokolü

**DHCP (Dynamic Host Configuration Protocol)**, ağa bağlanan cihazlara otomatik olarak IP ve diğer bilgileri atar.

### Atanan Bilgiler:

- IP adresi
- Subnet Mask
- Default Gateway
- DNS Sunucuları

> DHCP sunucusu bu bilgileri belirli bir süreliğine (lease time) atar.

---

## Güvenlik Duvarı (Firewall)

Amaç: Ağa gelen/giden trafiği denetleyerek güvenliği sağlamak.

### Özellikleri:

- Trafiği filtreler (IP, port, protokol bazlı)
- Kurallar tanımlanabilir
- Donanım veya yazılım tabanlı olabilir
- Genellikle **DMZ** ile birlikte çalışır


---

## ROUTER (Yönlendirici)

**Amaç:** Farklı ağlar arasında veri yönlendirmek.

### Özellikleri:

- IP adreslerine göre yönlendirir
- WAN bağlantısı sağlar
- Routing protokolleri: RIP, OSPF, BGP
- NAT, DHCP, güvenlik filtreleme gibi ek işlevler

> Router = A’dan B’ye veri gönderici + ağlar arası köprü

---

## SWITCH (Anahtar)

**Amaç:** Aynı ağ içindeki cihazları birbirine bağlar.

### Özellikleri:

- MAC adresi tabanlı çalışır
- Her cihaza özel bağlantı sağlar (collision domain yok)
- Layer 2 cihazıdır
- VLAN desteği sunar
- Layer 3 destekleyen modeller yönlendirme yapabilir

> Switch = Aynı ağ içindeki cihazları akıllıca bağlar.
