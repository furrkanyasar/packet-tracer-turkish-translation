# Cisco Packet Tracer - Türkçe Dil Paketi (Turkish Language Pack)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Metin Sayısı](https://img.shields.io/badge/Metin_Sayısı-10.303-blue.svg)](#)

Cisco Packet Tracer için hazırlanmış, **10.300+ arayüz ve yardım metnini kapsayan**, Qt tabanlı modern ve eksiksiz Türkçe dil paketi.

Ağ mühendisliği standartlarına (Cisco CCNA/CCNP müfredatı) ve doğal Türkçe dil bilgisine uygun olarak hazırlanmıştır.

---

## ⚡ Hızlı Kurulum (Tek Tıkla)

Packet Tracer'ın kurulu olduğu dizini aramanıza gerek kalmadan tek tıkla kurabilirsiniz:

1. Bu depoyu indirin (**Code > Download ZIP**).
2. ZIP dosyasını bir klasöre çıkartın.
3. Klasör içindeki **`install.bat`** dosyasına **çift tıklayın**.
4. Kurulum sihirbazı Packet Tracer kurulumunuzu otomatik olarak tespit edip dil paketini yükleyecektir.
5. Packet Tracer'ı açın:
   - **Options > Preferences > Administrative** (veya *Change Language*) menüsüne gidin.
   - Listeden **`tur.ptl`** (veya Turkish) seçeneğini seçip **Change Language** düğmesine tıklayın.
   - Packet Tracer'ı yeniden başlatın.

---

## 📁 Dosya Yapısı

| Dosya | Açıklama |
|---|---|
| **`install.bat`** | Tek tıkla otomatik kurulum sihirbazı |
| **`tur.ptl`** | Packet Tracer'ın doğrudan çalıştırdığı derlenmiş Türkçe dil paketi |
| **`tur.ts`** | Qt Linguist XML kaynak çeviri dosyası (düzenlenebilir kaynak metinler) |
| **`GLOSSARY.md`** | Cisco ve Ağ Terminolojisi Standartları Sözlüğü |
| **`LICENSE`** | MIT Açık Kaynak Lisansı |

---

## 📖 Terminoloji ve Çeviri Standartları

Çevirilerde tutarlılık sağlamak amacıyla [GLOSSARY.md](GLOSSARY.md) standartları benimsenmiştir:
* **Cisco IOS CLI Komutları Çevrilmez:** `show ip route`, `configure terminal`, `no shutdown`, `ip address` vb. doğrudan orijinal CLI formatında korunur.
* **Protokol İsimleri Korunur:** OSPF, EIGRP, BGP, VLAN, DHCP, DNS, STP, NAT, ACL vb.
* **Standart Donanım Terimleri:** Router ➔ *Yönlendirici*, Switch ➔ *Anahtar*, Default Gateway ➔ *Varsayılan Ağ Geçidi*, Subnet Mask ➔ *Alt Ağ Maskesi*.

---

## 🤝 Katkıda Bulunma

Hatalı gördüğünüz veya geliştirmek istediğiniz bir metin olursa:
1. `tur.ts` dosyasını bir metin editörüyle veya Qt Linguist ile açın.
2. İlgili çeviriyi düzenleyin.
3. Pull Request gönderin.

---

## 📄 Lisans

Bu proje **MIT Lisansı** ile paylaşılmıştır. Cisco Packet Tracer yazılımı Cisco Systems, Inc.'e aittir. Bu proje Cisco ile resmi bir bağlantıya sahip değildir.
