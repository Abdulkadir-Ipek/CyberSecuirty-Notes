#network #ag #cihaz #tespit #tarama
### Ağ Keşfi • Cihaz Tespiti • Pasif/Aktif Tarama

---

## 🔹 1. Temel Kavramlar

### ● Yerel Ağ (LAN)

- Aynı fiziksel ortamda bulunan, genellikle bir router veya switch aracılığıyla birbirine bağlı cihazlardan oluşur.
- Örnek: Ev veya ofis ağı.

### ● Dış Ağ (WAN / Internet)

- Yerel ağın dışındaki geniş ağları ifade eder.
- İnternet üzerindeki sunucular, uzak ofisler, diğer veri merkezleri gibi dış kaynaklar bu kapsamdadır.

---

## 🔹 2. Aktif Cihazları Tespit Etme Yöntemleri

### 🟠 A. Yerel Ağda Aktif Cihazları Bulma

#### 1. Ping Sweep

- IP aralığında tüm cihazlara ping atılır.

**Araçlar:**

- `ping`
- `nmap -sn 192.168.1.0/24`
- `fping`

#### 2. ARP Taraması

- MAC adresleri üzerinden cihazları keşfeder.
- [[net_ag_temelleri|Arp taraması burda gösteriliyor.]]

**Araçlar:**

- `arp -a` (Windows)
- `ip neigh` (Linux)
- `arp-scan`
- `Wireshark` (pasif)

#### 3. Nmap

- Gelişmiş tarama aracıdır.
- [[Techniques/tool_nmap|Nmap Kullanımı]]

**Komutlar:**

```bash
nmap -sn 192.168.1.0/24       # Ping sweep
nmap -sP 192.168.1.0/24       # Eski sürüm
nmap -sS 192.168.1.0/24       # TCP SYN taraması
```

#### 4. Netdiscover

- ARP tabanlı otomatik tarama.

#### 5. Router Arayüzü

- Bağlı cihazları doğrudan gösterir (genellikle 192.168.1.1 gibi bir IP üzerinden).


### 🟣 B. Dış Ağda (WAN) Aktif Cihazları Bulma

#### 1. Traceroute

- Paketlerin geçtiği yönlendiricileri listeler.

```bash 
traceroute google.com      # Linux tracert google.com         # Windows`
```

#### 2. Port Tarama (Nmap)


```bash
nmap -Pn -p 1-65535 example.com
```

#### 3. Shodan / Censys

- İnternette açık cihazları indeksleyen arama motorları.

#### 4. Whois / NSLookup / Dig

- Alan adı ve IP bilgisi toplamak için.

---

## 🔹 3. Pasif ve Aktif Tespit Yöntemleri

|Yöntem|Özellik|Avantaj|Dezavantaj|
|---|---|---|---|
|**Aktif**|Ağa sorgular gönderir|Hızlı|Tespit edilebilir|
|**Pasif**|Trafiği dinler|Gizli|Yavaş olabilir|

**Pasif araçlar:** Wireshark, tcpdump  
**Aktif araçlar:** Nmap, arp-scan, Netdiscover

---

## 🔹 4. Güvenlik ve Etik

- İzinsiz ağ taramaları yasal sorunlara yol açabilir.
- Yalnızca yetki sahibi olduğun ağlarda test yap.
- Kurumsal ortamlarda BT’den izin al.

---

## 🔹 5. Otomasyon ve Raporlama

### ● Otomasyon

- Bash / PowerShell script’leri ile zamanlanmış taramalar yapılabilir.
- Python ile: `scapy`, `nmap`, `os` modülleri kullanılabilir.

### ● Raporlama

```bash
nmap -oX scan.xml 192.168.1.0/24
```

- `.xml`, `.txt`, `.html` formatlarında rapor alınabilir.

---

## 🔹 6. Popüler Araçlar

|Araç|Açıklama|
|---|---|
|**Nmap**|Gelişmiş port ve cihaz tarayıcı|
|**Netdiscover**|Hızlı ARP tabanlı tarama|
|**arp-scan**|MAC adres keşfi|
|**Wireshark**|Pasif trafik analizörü|
|**Shodan**|İnternete açık cihaz tarayıcı|
|**Fing**|Mobil cihazlar için tarama aracı|

---

## 🔹 7. Örnek Senaryo – Yerel Ağ Taraması (Linux)


- Ağa bağlı tüm cihazları hızlıca taramak sudo nmap -sn 192.168.1.0/24  # MAC adresleriyle birlikte ARP taraması sudo arp-scan --interface=eth0 --localnet  # Trafiği pasif dinlemek (örneğin yeni cihazları tespit için) sudo wireshark

