#dns #network #ag 

DNS, **alan adlarını IP adreslerine çeviren** hiyerarşik ve dağıtık bir sistemdir.

İnternette “[google.com](http://google.com)” gibi isimleri, bilgisayarların anlayabileceği “142.250.74.206” gibi IP adreslerine dönüştürür.

---

### 🔧 DNS Nasıl Çalışır?

1. **Tarayıcıya adres yazılır:** `www.example.com`
2. **Yerel DNS önbelleği kontrol edilir.**
3. **Recursive resolver** sorguyu alır.
4. **Root sunucuya** istek gider.
5. **TLD sunucusu** (örneğin .com) yönlendirir.
6. **Authoritative DNS sunucu** doğru IP'yi verir.
7. Tarayıcı IP'ye bağlanır ve site açılır.

---

### 🧭 DNS Bileşenleri

|Bileşen|Görevi|
|---|---|
|**Recursive Resolver**|İstemciden sorgu alır, çözüm sürecini yönetir.|
|**Root Name Server**|.com, .net gibi TLD sunucularına yönlendirir.|
|**TLD Server**|Alan adının uzantısına göre yönlendirme yapar.|
|**Authoritative Server**|Nihai IP bilgisini sağlar.|

---

### 📂 DNS Kayıt Tipleri

|Kayıt Türü|Açıklama|
|---|---|
|**A**|Alan adını IPv4 adresine çevirir|
|**AAAA**|Alan adını IPv6 adresine çevirir|
|**CNAME**|Takma ad yönlendirmesi|
|**MX**|E-posta sunucularını belirtir|
|**NS**|Alan adı yetkili sunucularını gösterir|
|**TXT**|SPF, DKIM gibi metin verilerini içerir|
|**PTR**|IP'den alan adına çevirme (reverse DNS)|
|**SOA**|Alan adı otorite bilgileri|

---

### 🔍 DNS ile İlgili Komutlar

### 🖥️ Windows

- `nslookup example.com`
- `ipconfig /displaydns`

### 🖥️ Linux / macOS

- `dig example.com`
- `host example.com`
- `systemd-resolve --status` (Linux)

---

### 🔐 DNS Güvenliği

|Teknoloji|Açıklama|
|---|---|
|**DNSSEC**|DNS kayıtlarının dijital imzayla doğrulanması|
|**DoH**|DNS over HTTPS – şifreli DNS sorguları|
|**DoT**|DNS over TLS – TLS ile güvenli DNS|

---

### ⚠️ Yaygın DNS Problemleri

- **DNS cache poisoning:** Yanlış IP ile yönlendirme yapılması
- **DNS spoofing:** Sahte DNS cevaplarıyla kullanıcıyı kandırma
- **Yavaş sorgu süresi:** Yanıt süresinin uzun olması

---

### 🧠 DNS Kullanım Senaryoları

- Alan adı yönetimi
- Web barındırma (hosting)
- CDN yönlendirmeleri
- E-posta trafiği yönetimi
- Siber güvenlik (filtreleme, log analizi)