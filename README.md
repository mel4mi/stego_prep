# Stego Sorusu Hazırlama Dökümanı

**Bu döküman, basit seviyede stego soruları oluşturabilmeniz için rehberlik edecektir.**  
Steganografi (stego), dijital veriler içinde gizli bilgiler saklamanın eğlenceli ve öğretici bir yoludur. Bu döküman, metadata, görsel, ses dosyaları ve daha birçok teknikle gizleme yöntemlerini kapsar.


---

## Metadatalara Metin Saklamak

Metadata bilgilerini kullanarak basit bir şekilde metin saklayabilirsiniz.

### Gerekli Araçlar
- **ExifTool**: Metadata düzenlemek için.

### Kurulum ve Kullanım

**İndirmek:**
```bash
apt install exiftool
```

**Bir etiketi değiştirmek:**
```bash
exiftool -artist="mel4mi" foto.jpg
```

**Birden fazla etiketi değiştirmek:**
```bash
exiftool -artist="Muhammed Uzuner" -copyright="2024 Muhammed [mel4mi] Uzuner" foto.jpg
```

---

## JPG, BMP ve WAV Dosyalarına Metin/Dosya Saklamak

Steghide kullanarak bu dosyalara metin ya da dosya gömebilirsiniz.

### Kurulum ve Kullanım

**İndirmek:**
```bash
apt install steghide
```

**Metin/Dosya saklamak:**
```bash
steghide embed -ef gizli_metin.txt -cf foto.jpg
```

**Ayrıntılı kullanım için:**  
[Steghide: Beginner's Tutorial](https://systemweakness.com/steghide-a-beginners-tutorial-35ec0ea90446)

---

## PNG Dosyalarına Metin/Dosya Saklamak

### Gerekli Araçlar

- **iSteg**: PNG dosyalarına özel.

**İndirme ve kullanım detayları için:**  
[iSteg GitHub](https://github.com/rafiibrahim8/iSteg)

---

## Ses Dosyalarına Metin Saklamak

Ses dosyalarına mesaj gömmek için **HiddenWave** kullanabilirsiniz.

### Kurulum ve Kullanım

**İndirmek:**
[HiddenWave GitHub](https://github.com/techchipnet/HiddenWave)

**Metin saklamak:**
```bash
python3 HiddenWave.py -f muzik.wav -m "Çok gizli mesajım" -o cikti.wav
```

**Metni çıkarmak:**
```bash
python3 ExWave.py -f cikti.wav
```

---

## DTMF ile Saklama

DTMF tonları kullanarak bilgileri gizlemek için bu aracı kullanabilirsiniz:  
[DTMF Generator](https://onlinesound.net/dtmf-generator)

---

## Özel Sembollerle Şifreleme

Özel sembollerle şifreleme yapmak için kullanabileceğiniz bir araç:  
[Symbols Cipher Tool](https://www.dcode.fr/symbols-ciphers)

---

## Fotoğrafların Piksellerine Metin Saklamak

Fotoğrafların piksel düzeninde mesaj saklamak için **Npiet** kullanabilirsiniz:  
[Npiet](https://www.bertnase.de/npiet/npiet-execute.php)

---

## Fotoğraflara Metin/Şekil Yerleştirmek

Fotoğraf düzenleme araçlarıyla (ör. Adobe Photoshop veya GIMP) görsellerin üzerine metin veya şekil ekleyebilirsiniz.

---

## Şifre Seçimi

Stego işlemlerinde kullanılan şifreler **rockyou.txt** gibi yaygın parola listelerinde bulunmalıdır. Bu sayede sorunuz çözülmesi mümkün olan bir seviye sunar.

**İlk 100.000 şifreyi seçmek için:**
```bash
head -n 100000 rockyou.txt
```

---

## Hazırlık Adımları

1. Saklanacak metin veya dosyayı belirleyin.
2. Hangi saklama yöntemini kullanacağınıza karar verin.
3. Kullanılacak şifreyi seçin.
4. Gizleme işlemini test edin ve çözümü doğrulayın.
5. CTF için gerekli ipuçlarını hazırlayın.

---

**Daha fazlası için katkıda bulunabilirsiniz!**  
Bu döküman sizin yorumlarınız ve önerilerinizle büyüyebilir. Katkıda bulunmak için lütfen [GitHub repository](#) bağlantısını ziyaret edin.
