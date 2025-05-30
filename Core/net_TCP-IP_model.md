#ag #network #tcp #ip #tcp-ip #layer 
# TCP/IP Modeli

**TCP/IP (Transmission Control Protocol/Internet Protocol)**, modern internetin temelini oluşturan protokol takımıdır.  
OSI modelinden farklı olarak **4 katmandan** oluşur ve gerçek dünya internet iletişimi bu modele dayanır.

![[Pasted image 20250530204808.png]]

---

## 1. Uygulama Katmanı (Application Layer)

- **Görevi:** Kullanıcıya en yakın katmandır. Ağ hizmetlerini uygulamalara sunar.
- **OSI Karşılığı:** Oturum + Sunum + Uygulama Katmanları

**Protokoller:**  
HTTP/HTTPS, FTP, SMTP/POP3/IMAP, DNS, SSH, DHCP, SNMP

**Veri Biçimi:** `Mesaj (Message)`

---

## 2. Taşıma Katmanı (Transport Layer)

- **Görevi:** Uçtan uca veri iletimini yönetir. Hata kontrolü, bağlantı yönetimi sağlar.
- **OSI Karşılığı:** Taşıma Katmanı

### Protokoller:

- **TCP (Connection-Oriented):**
  - Güvenilir ve sıralı iletişim
  - `3-Way Handshake`: SYN → SYN-ACK → ACK
- **UDP (Connectionless):**
  - Hızlı ama güvenilir olmayan iletişim

**Port Örnekleri:**
- HTTP: 80, HTTPS: 443, DNS: 53, FTP: 21

**Veri Biçimi:** `Segment (TCP)` / `Datagram (UDP)`

---

## 3. İnternet Katmanı (Internet Layer)

- **Görevi:** Yönlendirme (routing) ve adresleme yapar.
- **OSI Karşılığı:** Ağ Katmanı

**Protokoller:**
- **IP (IPv4, IPv6):** Temel yönlendirme
- **ICMP:** Hata iletimi, ping/traceroute
- **ARP:** IP → MAC çevirisi
- **RIP, OSPF, BGP:** Yönlendirme protokolleri

**Veri Biçimi:** `Paket (Packet)`

---

## 4. Ağ Erişim Katmanı (Network Access Layer)

- **Görevi:** Fiziksel ağ üzerinden veri iletimi sağlar.
- **OSI Karşılığı:** Fiziksel + Veri Bağlantı Katmanları

**Teknolojiler:**
- Ethernet (802.3), Wi-Fi (802.11), PPP

**Donanımlar:**  
Switch, hub, kablo, modem

**Veri Biçimi:** `Çerçeve (Frame)`

---

## TCP/IP Veri Akışı (Encapsulation)

### Gönderici Tarafta:
1. **Uygulama:** HTTP mesajı hazırlanır.
2. **Taşıma:** TCP başlığı (port numaraları) eklenir.
3. **İnternet:** IP başlığı (IP adresleri) eklenir.
4. **Ağ Erişim:** MAC adresleri ile frame oluşturulur.

### Alıcı Tarafta:
1. **Ağ Erişim:** MAC adresi kontrol edilir.
2. **İnternet:** IP adresi değerlendirilir.
3. **Taşıma:** Port numarasına göre uygulamaya yönlendirilir.
4. **Uygulama:** HTTP yanıtı işlenir.

---

## TCP/IP Özellikleri

- **Modülerlik:** Katmanlar bağımsızdır.
- **Ölçeklenebilirlik:** Küresel ağları destekler.
- **Güvenlik:** SSL/TLS (üst katmanlarda), IPsec (internet katmanında)
- **Adresleme:** IPv4 ve IPv6 desteği

---

## TCP/IP vs OSI

| Özellik            | TCP/IP       | OSI               |
|--------------------|--------------|--------------------|
| Katman Sayısı       | 4            | 7                  |
| Kullanım Durumu     | Pratik/gerçek | Teorik model       |
| Tanım Şekli         | Protokollerle | İşlevlerle         |

---

## Ek Kavramlar

- **NAT:** Özel IP’leri genel IP’ye çevirir.
- **Socket:** IP + Port (örn: `192.168.1.1:443`)
- **Router:** İnternet katmanında çalışır.
- **TCP Handshake:** Bağlantı kurulumu (SYN → SYN-ACK → ACK)

---

## Gerçek Hayat Örneği: Web Sitesi Ziyareti

1. **Tarayıcıya** `www.google.com` yazılır.
2. **DNS**, alan adını IP’ye çevirir → **Uygulama Katmanı**
3. **TCP bağlantısı kurulur** → **Taşıma Katmanı**
4. **IP paketleri yönlendirilir** → **İnternet Katmanı**
5. **Fiziksel iletim sağlanır** (Ethernet/Wi-Fi) → **Ağ Erişim Katmanı**

---
