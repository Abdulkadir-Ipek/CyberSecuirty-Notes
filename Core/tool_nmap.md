#tool #tools #nmap #scan 

# 🧠 NMAP CHEAT SHEET 📄

### Ağ Keşfi • Port Taraması • Servis Analizi • Güvenlik Testi

---

## 🔍 TEMEL TARAMALAR

| Komut | Açıklama |
|-------|----------|
| `nmap <ip>` | Temel tarama (varsayılan 1000 port) |
| `nmap -sn <ip>` | Ping taraması (host discovery) |
| `nmap <ip1> <ip2>` | Birden fazla hedef |
| `nmap <ip-range>` | IP aralığı tarama (örn: 192.168.1.1-100) |
| `nmap -iL list.txt` | Dosyadan hedef listesi oku |
| `nmap -p- <ip>` | Tüm 65535 portu tara |

---

## 🔐 PORT TARAMA TÜRLERİ

| Seçenek             | Açıklama                              |
| ------------------- | ------------------------------------- |
| `-sS`               | SYN (stealth) taraması                |
| `-sT`               | TCP connect() (tam bağlantı)          |
| `-sU`               | UDP port taraması                     |
| `-sN`, `-sF`, `-sX` | Firewall atlatma için sinsi taramalar |

---

## ⚙️ SERVİS VE OS BİLGİSİ

| Seçenek | Açıklama |
|---------|----------|
| `-sV` | Servis ve versiyon bilgisi |
| `-O` | İşletim sistemi tespiti |
| `--osscan-guess` | OS tahminini zorla |
| `-A` | Hepsi bir arada: OS + Versiyon + Script + Traceroute |

---

## 📡 NSE (Nmap Scripting Engine)

| Komut | Açıklama |
|-------|----------|
| `--script=default` | Varsayılan scriptler |
| `--script=vuln` | Bilinen açıklıkları tarar |
| `--script=http-enum` | Web servis analizleri |
| `--script-help <script>` | Script hakkında bilgi al |

> 📂 Script dizini: `/usr/share/nmap/scripts/`

---

## ⏱️ HIZ ve ZAMANLAMA

| Seçenek | Açıklama |
|---------|----------|
| `-T0` ila `-T5` | Tarama hızı (0: çok yavaş, 5: çok hızlı) |
| `--min-rate 1000` | Saniyede en az 1000 paket gönder |
| `--max-retries 2` | Zaman aşımı tekrar sayısı |

---

## 🎯 HEDEF SEÇİMİ

| Seçenek | Açıklama |
|---------|----------|
| `-Pn` | Ping atlamadan doğrudan tara |
| `-n` | DNS çözümlemesini kapat |
| `-R` | Ters DNS çözümlemesini zorla |

---

## 💾 ÇIKTI FORMATLARI

| Komut | Açıklama |
|-------|----------|
| `-oN çıktı.txt` | Normal metin çıktısı |
| `-oG çıktı.gnmap` | Grep ile analiz edilebilir çıktı |
| `-oX çıktı.xml` | XML formatı |
| `-oA çıktı` | Yukarıdaki 3 formatı birlikte kaydeder |

---

## 🎯 ÖRNEK KOMUTLAR

```bash
nmap -A -T4 192.168.1.1
# Geniş kapsamlı, hızlı tarama

nmap -sS -p 22,80,443 -T3 10.0.0.1
# Belirli portlarda stealth tarama

nmap --script vuln 192.168.1.10
# Güvenlik açığı taraması

nmap -sU -p 53 192.168.1.5
# UDP DNS portu taraması
