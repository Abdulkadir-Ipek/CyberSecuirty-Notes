#linux #kali #dosya #sistem 
# Kali Linux Temel Komutlar ve Araçlar

Kali Linux, sızma testleri ve bilgi güvenliği analizleri için geliştirilmiş bir Debian tabanlı dağıtımdır. Aşağıda, Kali üzerinde sıkça kullanılan komutlar ve araçlar listelenmiştir.

## 🛠️ Sistem ve Kullanıcı Bilgisi

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| uname -a | Sistem çekirdeği ve mimari bilgisi | `uname -a` |
| lsb_release -a | Dağıtım bilgisi | `lsb_release -a` |
| whoami | Anlık kullanıcı adını gösterir | `whoami` |
| id | Kullanıcının UID, GID bilgilerini verir | `id` |
| passwd | Şifre değiştirme | `passwd` |
| hostname | Sistem adı görüntüleme veya ayarlama | `hostname` |

---

## 💽 Dosya ve Disk İşlemleri

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| lsblk | Bağlı blok aygıtlarını gösterir | `lsblk` |
| fdisk | Disk bölümlerini düzenler | `sudo fdisk -l` |
| mount / umount | Disk bağlama / çıkarma | `mount /dev/sdb1 /mnt` |
| df -h | Disk kullanımı (insan okunur) | `df -h` |
| du -sh | Dizin boyutu | `du -sh Downloads/` |

---

## 📡 Ağ Analizi ve Bağlantılar

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| ifconfig / ip a | Ağ arayüzü bilgisi | `ip a` |
| iwconfig | Kablosuz ağ yapılandırması | `iwconfig wlan0` |
| ping | Ağ bağlantısını test eder | `ping 8.8.8.8` |
| netstat / ss | Bağlantı bilgisi (ss daha moderndir) | `ss -tuln` |
| traceroute | Hedefe giden ağ yolunu gösterir | `traceroute google.com` |

---

## 🔐 Sızma Testi ve Güvenlik Araçları

| Araç | Açıklama | Örnek Kullanım |
|------|----------|----------------|
| nmap | Ağ keşif ve port taraması | `nmap -sS 192.168.1.1` |
| netdiscover | LAN üzerindeki cihazları tespit eder | `netdiscover` |
| wireshark | Grafiksel paket analiz aracı | `wireshark` |
| tcpdump | CLI tabanlı trafik izleyici | `tcpdump -i eth0` |
| hydra | Brute-force saldırı aracı | `hydra -l admin -P pass.txt ssh://192.168.1.10` |
| john | Şifre kırma aracı | `john --wordlist=rockyou.txt hashes.txt` |
| aircrack-ng | Kablosuz ağ kırma aracı | `aircrack-ng capture.cap` |

---

## 🧰 Bilgi Toplama (Recon)

| Araç | Açıklama | Örnek Kullanım |
|------|----------|----------------|
| whois | Alan adı bilgisi | `whois example.com` |
| dig / nslookup | DNS çözümleme araçları | `dig google.com` |
| theHarvester | E-posta, alt alan, isim toplar | `theHarvester -d target.com -b google` |
| whatweb | Web sunucusu ve uygulama tespiti | `whatweb example.com` |
| recon-ng | Modüler bilgi toplama framework’ü | `recon-ng` |

---

## ⚙️ Hizmet ve Süreç Yönetimi

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| systemctl | Servis yönetimi | `systemctl restart ssh` |
| service | Eski sistemlerde servis yönetimi | `service apache2 status` |
| ps aux | Aktif süreçler | `ps aux | grep python` |
| htop | Renkli ve etkileşimli işlem izleyici | `htop` |
| kill / killall | PID’ye veya isme göre işlem sonlandırma | `killall firefox` |

---

## 📦 Paket Yönetimi

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| apt update | Paket listelerini günceller | `sudo apt update` |
| apt upgrade | Sistem paketlerini yükseltir | `sudo apt upgrade` |
| apt install | Yeni paket kurar | `sudo apt install nmap` |
| apt remove | Paket kaldırır | `sudo apt remove wireshark` |

---

## 🗃️ Dosya İşlemleri ve Metin Araçları

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| find | Dosya/dizin arar | `find / -name passwd` |
| locate | Hızlı dosya araması | `locate sshd_config` |
| grep | Metin içinde desen arar | `grep "root" /etc/passwd` |
| cut, sort, uniq | Metin işleme | `cut -d: -f1 /etc/passwd` |
| cat, less, head, tail | Dosya görüntüleme araçları | `tail -f /var/log/syslog` |

---

## 🧪 Terminal Temizliği ve Yardım

| Komut | Açıklama | Örnek Kullanım |
|-------|----------|----------------|
| clear | Terminali temizler | `clear` |
| history | Komut geçmişi | `history | grep ssh` |
| man | Komutların yardım kılavuzu | `man nmap` |
| --help | Komutun kısa yardım çıktısı | `nmap --help` |

---

> ✅ **Not:** Kali Linux'ta çoğu saldırı aracı root yetkisi gerektirir. `sudo` veya doğrudan `root` terminali kullanmak yaygındır.

---

