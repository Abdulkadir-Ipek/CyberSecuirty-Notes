#osi #ag #network #layer
# OSI Modeli

**OSI (Open Systems Interconnection)** modeli, ağ iletişimini 7 katmana ayıran kavramsal bir çerçevedir.  
Her katman, belirli bir görevi üstlenir ve üst katmana hizmet sağlar.

## Ana Katmanlar

- **7. Uygulama Katmanı:** Son kullanıcı uygulamalarıyla doğrudan etkileşim kurar
- **6. Sunum Katmanı:** Veri biçimlendirme ve şifreleme işlemlerini gerçekleştirir
- **5. Oturum Katmanı:** Bağlantı yönetimi ve oturum kontrolünü sağlar
- **4. Taşıma Katmanı:** Uçtan uca iletişim ve güvenilir veri aktarımını yönetir
- **3. Ağ Katmanı:** Yönlendirme ve mantıksal adresleme işlevlerini yerine getirir
- **2. Veri Bağlantı Katmanı:** Fiziksel adresler ve hata kontrolü ile ilgilenir
- **1. Fiziksel Katman:** Fiziksel ortam üzerinden bit iletimini sağlar

## Katmanlar

### 7. Uygulama Katmanı (Application Layer)

- Kullanıcıya en yakın katmandır.
- Ağ servislerini uygulamalara sunar.

**Protokoller:**  
HTTP/HTTPS, FTP, SMTP/POP3, DNS  
**Uygulamalar:**  
Tarayıcılar, Outlook, Zoom

---

### 6. Sunum Katmanı (Presentation Layer)

- Veriyi uygulama katmanına uygun formata dönüştürür.
- Şifreleme, sıkıştırma, kod dönüşümleri yapar.

**Örnekler:**  
SSL/TLS, JPEG, MPEG, ASCII ↔ Unicode dönüşümü

---

### 5. Oturum Katmanı (Session Layer)

- Oturumların kurulması, yönetilmesi ve sonlandırılmasından sorumludur.

**Örnekler:**  
NetBIOS, RPC, VPN oturumları

---

### 4. Taşıma Katmanı (Transport Layer)

- Uçtan uca iletişimi ve veri güvenliğini sağlar.
- Segmentasyon, akış kontrolü, hata düzeltme gibi işlevler üstlenir.

**Protokoller:**

- **TCP:** Güvenilir, bağlantı tabanlı
- **UDP:** Hızlı, bağlantısız

**Port Numaraları:**  
HTTP (80), HTTPS (443), DNS (53)

---

### 3. Ağ Katmanı (Network Layer)

- Paketleri yönlendirir (routing) ve IP adresleriyle adresleme yapar.

**Cihazlar:** Router  
**Protokoller:** IP, ICMP, OSPF, BGP  
**Adresleme:** IPv4, IPv6

---

### 2. Veri Bağlantı Katmanı (Data Link Layer)

- Veriyi çerçeve (frame) haline getirir ve fiziksel katmana iletir.
- MAC adresleriyle çalışır, hata kontrolü sağlar.

**Alt Katmanlar:**
- **LLC:** Hata kontrolü, akış yönetimi
- **MAC:** Ortam erişimi

**Cihazlar:** Switch, Bridge  
**Protokoller:** Ethernet, Wi-Fi, PPP, ARP

---

### 1. Fiziksel Katman (Physical Layer)

- Bit düzeyinde iletim yapar; sinyaller üzerinden çalışır.

**Örnekler:**  
Kablolar, hub’lar, repeater’lar  
**Teknikler:**  
Voltaj, pin yapısı, bant genişliği  
**Protokoller:**  
Ethernet (fiziksel seviye), USB, Bluetooth

---

## OSI İşleyişi: Veri Akışı

### 1. Encapsulation (Veri Paketleme)

Veri yukarıdan aşağıya her katmanda başlık (header) alır:

Uygulama verisi → TCP başlığı → IP başlığı → MAC başlığı → Bitler

### 2. Decapsulation (Veri Çözme)

Alıcı cihaz, veriyi aşağıdan yukarıya doğru çözümler, her katmanda başlıkları sırasıyla çıkarır.

---


