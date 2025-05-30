#tool #tools #wireshark #tarama #izleme
### 📌 Nedir?

Wireshark, ağ trafiğini analiz etmek için kullanılan açık kaynaklı ve güçlü bir **protokol analizörüdür**. Gerçek zamanlı olarak ağ paketlerini yakalayabilir, çözümleyebilir ve detaylı incelemeler yapmanı sağlar.

---

### 🔧 Temel Özellikler

- Gerçek zamanlı ağ trafiği yakalama
- Çeşitli protokolleri çözümleme (HTTP, TCP, DNS, ARP, vs.)
- Filtreleme, renk kodlama ve paket detaylarını inceleme
- PCAP dosyalarını açma ve analiz etme
- GUI arayüzüyle kullanım kolaylığı

---

### 🖥️ Kurulum

- **Windows**: [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html)
- **Linux**: `sudo apt install wireshark`
- **macOS**: `brew install wireshark`

---

### 📂 Paket Yakalama

1. Wireshark'ı aç
2. Ağ arayüzünü seç (örneğin: `eth0`, `wlan0`)
3. “Start Capturing”e tıkla
4. Canlı trafiği izle

---

### 🔍 Yaygın Görülen Protokoller

|Protokol|Açıklama|
|---|---|
|HTTP|Web trafiği|
|DNS|Alan adı çözümleme|
|TCP|Bağlantı odaklı veri aktarımı|
|UDP|Hızlı, bağlantısız aktarım|
|ARP|MAC adresi çözümlemesi|
|ICMP|Ping, hata mesajları|

---

### 🔎 Filtreleme (Display Filters)

### 📄 Temel Filtre Örnekleri:

- `ip.addr == 192.168.1.1` → Belirli IP adresi
- `tcp.port == 80` → Belirli port
- `http` → Yalnızca HTTP trafiği
- `dns` → Yalnızca DNS paketleri
- `tcp.flags.syn == 1` → SYN bayrağı aktif TCP paketleri

### 🧠 Kullanışlı Filtreler:

- `tcp contains "login"` → Paket içinde "login" kelimesi geçen TCP trafiği
- `frame contains "password"` → Parola içeren veri arama
- `ip.src == 192.168.1.100 && tcp.port == 443` → Belirli IP’den gelen HTTPS trafiği

---

### 📌 Kısa Yol Tuşları

|Tuş|İşlev|
|---|---|
|Ctrl + E|Başlat/Durdur yakalama|
|Ctrl + F|Arama|
|Ctrl + H|Filtreleme geçmişi|
|Ctrl + /|Tüm filtreleri temizle|
|Shift + Ctrl + P|Tercihler|

---

### 📁 Kayıt ve Dışa Aktarma

- `File > Save As` ile PCAP formatında kayıt
- `Export Packet Dissections` ile CSV, JSON, plain text formatlarında dışa aktarım

---

### 🧠 İpuçları

- Renk kodlamaları ile farklı protokolleri ayırt edebilirsin
- "Follow TCP Stream" özelliği ile oturumun tamamını tek ekranda görebilirsin
- Ağ güvenliği, şüpheli trafik veya parola analizi için idealdir