#network #ag #http #web 
HTTP, istemci (genellikle web tarayıcısı) ile sunucu arasında **veri iletimini sağlayan uygulama katmanı protokolüdür**. Web sayfalarının yüklenmesinde kullanılır.

---

### 🔧 HTTP Nasıl Çalışır?

1. **İstemci**, bir web adresi talep eder (`example.com`).
2. **DNS**, alan adını IP adresine çevirir.
3. **Tarayıcı**, sunucuya bir HTTP isteği gönderir.
4. **Sunucu**, ilgili cevabı (örneğin bir HTML sayfası) gönderir.
5. **Tarayıcı**, içeriği kullanıcıya gösterir.

---

### 🔄 HTTP İstek Yöntemleri (Request Methods)

|Yöntem|Açıklama|
|---|---|
|**GET**|Veri alma (sayfa, resim, dosya vs.)|
|**POST**|Sunucuya veri gönderme (form, API vs.)|
|**PUT**|Var olan veriyi güncelleme|
|**DELETE**|Veriyi silme|
|**HEAD**|Yalnızca başlık bilgilerini alır (body yok)|
|**OPTIONS**|Sunucunun desteklediği yöntemleri listeler|
|**PATCH**|Verinin küçük bir kısmını günceller|

---

### 📥 HTTP Yanıt Kodları (Status Codes)

|Kategori|Kodu|Anlamı|
|---|---|---|
|✅ Başarılı|200 OK|İstek başarılı|
|🔄 Yönlendirme|301 / 302|Kalıcı / Geçici yönlendirme|
|❗ Hata (istemci)|400 / 401 / 403 / 404|Hatalı istek, yetkisiz, yasaklı, bulunamadı|
|💥 Hata (sunucu)|500 / 502 / 503|Sunucu hataları|

---

### 🔐 HTTP vs HTTPS

|Özellik|HTTP|HTTPS|
|---|---|---|
|Şifreleme|Yok|Var (SSL/TLS ile)|
|Güvenlik|Düşük|Yüksek|
|Port|80|443|
|Kullanım|Test, güvenli olmayan|Gerçek, hassas veri içeren|

---

### 🧱 HTTP Yapısı

### 📨 İstek (Request)

```
GET /index.html HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
```

### 📩 Yanıt (Response)

```
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 2048
```

_(+ body kısmı: HTML içeriği)_

---

### 📁 HTTP Başlıkları (Headers)

### 🔼 İstek Başlıkları

|Başlık|Açıklama|
|---|---|
|Host|Hedef sunucu|
|User-Agent|Tarayıcı bilgisi|
|Accept|Kabul edilen içerik türleri|
|Authorization|Kimlik doğrulama verisi|

### 🔽 Yanıt Başlıkları

|Başlık|Açıklama|
|---|---|
|Content-Type|Dönen içeriğin türü|
|Set-Cookie|Tarayıcıya cookie gönderimi|
|Cache-Control|Önbellekleme kuralları|
|Server|Sunucu bilgisi|

---

### 🧠 HTTP Hakkında Bilinmesi Gerekenler

- **Stateless**: Her istek bağımsızdır, bağlantı durumu korunmaz.
- **URL** (Uniform Resource Locator): HTTP'nin eriştiği adres biçimidir.
- **Cookie / Session** gibi mekanizmalarla oturum bilgisi taşınabilir.
- REST API’ler genellikle HTTP üzerinden çalışır.