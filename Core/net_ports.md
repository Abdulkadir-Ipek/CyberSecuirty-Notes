#network #ag #portlar #ports
# 🔢 Yaygın Port Numaraları ve Hizmetleri

Aşağıda sık kullanılan TCP/UDP port numaraları ve bu portlarda çalışan protokoller/hizmetler listelenmiştir. Bu bilgiler, ağ güvenliği, tarama analizi ve firewall yapılandırmaları gibi konularda sıklıkla kullanılır.

---

## 📌 Temel Port Listesi

| Port No | Protokol | Hizmet / Açıklama |
|---------|----------|--------------------|
| 20      | TCP      | FTP (Data Transfer) |
| 21      | TCP      | FTP (Control / Login) |
| 22      | TCP      | SSH (Secure Shell) |
| 23      | TCP      | Telnet (Uzak oturum – güvenli değil) |
| 25      | TCP      | SMTP (E-posta gönderme) |
| 53      | TCP/UDP  | DNS (Alan adı çözümleme) |
| 67      | UDP      | DHCP (Sunucu – IP dağıtımı) |
| 68      | UDP      | DHCP (İstemci) |
| 69      | UDP      | TFTP (Basit dosya aktarımı) |
| 80      | TCP      | HTTP (Web siteleri) |
| 110     | TCP      | POP3 (E-posta alma) |
| 123     | UDP      | NTP (Zaman senkronizasyonu) |
| 137–139 | TCP/UDP  | NetBIOS (Windows paylaşım hizmetleri) |
| 143     | TCP      | IMAP (E-posta alma) |
| 161     | UDP      | SNMP (Ağ cihaz yönetimi) |
| 389     | TCP/UDP  | LDAP (Dizin hizmetleri) |
| 443     | TCP      | HTTPS (Güvenli web erişimi) |
| 445     | TCP      | SMB (Dosya ve yazıcı paylaşımı) |
| 514     | UDP      | Syslog (Log iletimi) |
| 587     | TCP      | SMTP (TLS ile e-posta gönderme) |
| 631     | TCP/UDP  | IPP (Yazıcı paylaşımı) |
| 993     | TCP      | IMAPS (SSL ile IMAP) |
| 995     | TCP      | POP3S (SSL ile POP3) |
| 1433    | TCP      | Microsoft SQL Server |
| 1521    | TCP      | Oracle DB |
| 3306    | TCP      | MySQL |
| 3389    | TCP      | RDP (Uzak masaüstü bağlantısı) |
| 5432    | TCP      | PostgreSQL |
| 5900    | TCP      | VNC (Uzak masaüstü erişimi) |
| 8080    | TCP      | HTTP Alternatif Port (proxy/web) |

---

## 💡 Notlar

- `TCP` genellikle bağlantı tabanlı ve güvenilir iletişim sağlar.
- `UDP` bağlantısız ve hızlı iletişim için kullanılır (örneğin DNS, NTP).
- Port tarama yaparken bu portların açık olup olmadığını kontrol etmek, bir servisin varlığı hakkında bilgi verebilir.
- Güvenlik duvarlarında bu portlara göre filtreleme yapılabilir.

---
