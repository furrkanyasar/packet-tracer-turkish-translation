# Cisco Packet Tracer - Ağ Terminolojisi ve Yerelleştirme Sözlüğü (Glossary)

Bu belge; **Cisco Packet Tracer Türkçe Dil Paketi** projesinde kullanılan teknik ağ terminolojisi, yazılım arayüzü eylem standartları, protokol kuralları ve yerelleştirme kılavuzudur. 

Çevirilerde tutarlılık sağlamak amacıyla tüm metinler bu sözlükteki standartlara göre düzenlenmiştir.

---

## 📌 1. Temel Yerelleştirme İlkeleri

1. **Cisco IOS CLI Komutları ve Çıktıları ASLA Çevrilmez:**
   * Örnek: `show ip route`, `configure terminal`, `interface FastEthernet0/1`, `no shutdown`, `switchport mode access`, `ip address`, `router ospf` doğrudan orijinal CLI formatında korunur.
2. **Runtime Token ve Değişken Güvenliği (`[[...]]` & `%n`):**
   * Packet Tracer motorunun çalışma zamanında aradığı `[[variablename]]`, `[[query-type]]`, `[[Name]]`, `[[PORT]]`, `[[SIZE]]`, `[[IP]]`, `[[FLAGS]]` gibi token'lar **kesinlikle çevrilmez**.
   * `%1`, `%2` gibi Qt değişkenlerinin sırası cümle yapısına göre değişebilir ancak değişken isimleri bozulmaz.
   * Yüzdelik ifadelerin (`%100`, `%50`) Qt tarafından değişken sanılmaması için `% 100` veya `%%100` formatı kullanılır.
3. **Standart Eylem Ayrımı:**
   * `Delete` ➔ **Sil** *(Kalıcı veri silme)*
   * `Remove` ➔ **Kaldır** *(Listeden veya panelden çıkarma)*
   * `Disconnect` ➔ **Bağlantıyı Kes** *(Eylem / Fiil)*
   * `Disconnected` ➔ **Bağlantı Kesildi** *(Durum / Sıfat)*

---

## 🔀 2. Yönlendirme ve Anahtarlama (Routing & Switching)

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama ve Kullanım Notları |
|---|---|---|
| **Router** | Yönlendirici | Temel ağ yönlendirme cihazı |
| **Switch** | Anahtar | Katman 2/Katman 3 anahtarlama cihazı |
| **Routing / Routes** | Yönlendirme / Rotalar | "Yol" yerine teknik ağ terimi olan **"Rota"** kullanılır |
| **Routing Table** | Yönlendirme Tablosu | Cihaz üzerindeki rota tablosu |
| **Default Route** | Varsayılan Rota | `0.0.0.0/0` rotası |
| **Default Information Originate** | Varsayılan Bilgi Yayını (Default Information Originate) | OSPF/yönlendirme varsayılan rota yayını |
| **Successor** | Successor | EIGRP birincil yönlendirici terimi (halef) |
| **Feasible Successor** | Feasible Successor | EIGRP yedek yönlendirici terimi |
| **Hello Interval** | Hello Aralığı | OSPF/EIGRP Hello paket zamanlayıcısı ("Selam" yapılmaz) |
| **Dead Interval** | Dead Aralığı | OSPF komşuluk düşme zamanlayıcısı |
| **VTP (VLAN Trunking Protocol)** | VTP | Protokol adı korunur |
| **Summary / Subset Advertisement** | Özet / Alt Küme Duyurusu | VTP/yönlendirme mesajları ("İlan" yerine **"Duyuru"**) |
| **Router Advertisement (RA)** | Yönlendirici Duyurusu | IPv6 ND/SLAAC duyurusu |
| **Native VLAN** | Native VLAN (Yerel VLAN) | 802.1Q etiketsiz VLAN |
| **Trunk / Trunk Port** | Trunk / Trunk Portu | Çoklu VLAN taşıyan port |
| **Access Port** | Erişim Portu | Tek VLAN'a bağlı uç kullanıcı portu |
| **SwitchPort** | Switch Portu (SwitchPort) | Anahtar arayüzü ayarı |
| **Frame Relay** | Frame Relay | WAN protokol adı korunur |
| **Spanning Tree Protocol (STP)** | Kapsayan Ağaç Protokolü (STP) | Katman 2 döngü önleme protokolü |
| **Bridge Protocol Data Unit (BPDU)**| BPDU | STP kontrol çerçevesi |

---

## 🔐 3. Güvenlik, Kimlik Doğrulama ve AAA

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama ve Kullanım Notları |
|---|---|---|
| **Enable Secret** | Enable Secret Parolası | Cisco Privileged EXEC yetkili şifreli parolası |
| **Service Password Encryption** | Service Password Encryption (Hizmet Parolası Şifrelemesi) | Düz metin parolaları şifreleyen IOS hizmeti |
| **Shared Secret** | Paylaşılan Gizli Parola | RADIUS/TACACS+ paylaşılan parolası |
| **AAA (Authentication, Authorization, Accounting)** | AAA (Kimlik Doğrulama, Yetkilendirme, Muhasebe) | Cisco AAA çerçevesi |
| **Accounting** | Muhasebe (Accounting) | Denetim ve kayıt tutma ("Hesaplama" yapılmaz) |
| **Passphrase / Pass Phrase** | Parola İfadesi | WPA/WPA2 anahtarı veya güvenlik cümlesi |
| **Password** | Parola | Giriş parolaları ("Şifre" kriptografi için ayrılmıştır) |
| **Encryption / Cipher** | Şifreleme | Kriptografik veri koruma işlemi |
| **802.1X / dot1x** | 802.1X | Port tabanlı ağ erişim kontrol standardı |
| **Access Control List (ACL)** | Erişim Kontrol Listesi (ACL) | Paket filtreleme kuralları |
| **Port Security** | Port Güvenliği / Bağlantı Noktası Güvenliği | MAC adresi sınırlandırma özelliği (UI ve CLI bağlamı) |

---

## 🌐 4. Temel Ağ Kavramları ve IP Mimarisi

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama ve Kullanım Notları |
|---|---|---|
| **Default Gateway** | Varsayılan Ağ Geçidi | Yerel ağdan dış ağa çıkış IP'si |
| **Subnet Mask** | Alt Ağ Maskesi | IP adresini ağ ve ana bilgisayar kısmına ayıran maske |
| **Link-Local Address** | Link-Local Adresi (Bağlantı-Yerel) | `FE80::/10` veya `169.254.0.0/16` yerel adresi |
| **Broadcast** | Yayın / Genel Yayın | Ağdaki tüm cihazlara gönderim |
| **Unicast** | Teke Gönderim (Unicast) | Tek bir hedefe gönderim |
| **Multicast** | Çoka Gönderim (Multicast) | Belirli bir abone grubuna gönderim |
| **Broadcast Storm Control** | Broadcast Storm Denetimi | Yayın fırtınası önleme mekanizması |
| **Throughput** | İş Hacmi / Verim | Birim zamanda iletilen gerçek veri miktarı |
| **Bandwidth** | Bant Genişliği | Hattın maksimum veri taşıma kapasitesi |
| **Latency / Delay** | Gecikme | Verinin kaynaktan hedefe ulaşma süresi |
| **Payload** | Veri Yükü (Payload) | Paketin taşıdığı asıl kullanıcı verisi |
| **Hash Table** | Hash Tablosu | Bilgisayar bilimi veri yapısı ("Karma tablo" yapılmaz) |

---

## 🏢 5. Fiziksel Donanım, Kabin ve Kablolama

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama ve Kullanım Notları |
|---|---|---|
| **Rack** | Kabin (Rack) | Sistem cihazlarının takıldığı ağ kabini ("Raf" yapılmaz) |
| **Shelf (Inventory Shelf)** | Envanter Rafı | Cihazların durduğu raf |
| **Table** | Masa | Fiziksel çalışma alanındaki çalışma masası |
| **Straight-Through Cable** | Düz Kablo | Farklı türdeki cihazları bağlayan bakır kablo |
| **Crossover Cable** | Çapraz Kablo | Benzer cihazları bağlayan bakır kablo |
| **Fiber Optic** | Fiber / Fiber Optik | Yüksek hızlı optik kablo |
| **Console Cable** | Konsol Kablosu | Cihaz yönetimi için kullanılan mavi kablo |
| **Fast Ethernet** | Fast Ethernet | 100 Mbps Ethernet port/teknolojisi |
| **Gigabit Ethernet** | Gigabit Ethernet | 1000 Mbps Ethernet port/teknolojisi |
| **Coverage Range** | Kapsama Menzili | Kablosuz sinyal alanı ("metre / fit") |
| **Beacon Interval / Frequency** | Beacon Aralığı / Frekansı | AP sinyal yayma periyodu |

---

## 📊 6. Simülasyon, Olaylar ve PDU Paneli

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama ve Kullanım Notları |
|---|---|---|
| **PDU (Protocol Data Unit)** | PDU (Protokol Veri Birimi) | Katmanlar arası taşınan veri birimi |
| **Capture then Forward** | Yakala ve İlet | Simülasyon paneli tek adım ilerletme eylemi |
| **In Progress** | Devam Ediyor | Devam eden paket veya işlem durumu |
| **Event List** | Olay Listesi | Simülasyon adım geçmişi tablosu |
| **Inbound PDU** | Gelen PDU | Cihaza giriş yapan paket |
| **Outbound PDU** | Giden PDU | Cihazdan çıkış yapan paket |

---

## 🖱️ 7. Yazılım Arayüzü (UI) Buton ve Eylem Standartları

| İngilizce Terim | Türkçe Standart Karşılık | Açıklama |
|---|---|---|
| **Rename** | Yeniden Adlandır | Tüm diyalog ve dosya yöneticilerinde standarttır |
| **Remove** | Kaldır | Listeden veya tablodan çıkarma |
| **Delete** | Sil | Kalıcı olarak silme |
| **Dialog** | İletişim Kutusu | Açılır pencere/diyalog |
| **Scripting** | Komut Dosyası | Packet Tracer script arayüzü |
| **Tether** | İnternet Paylaşımı | Bluetooth/mobil tethering |
| **Untether** | İnternet Paylaşımını Sonlandır | Tethering bağlantısını kapatma |
| **Upgrade Firmware** | Firmware'i Yükselt | Cihaz yazılımı güncelleme |
| **Wireless Mode** | Kablosuz Modu | 802.11 b/g/n modu |
| **Cancel** | İptal | İptal düğmesi |
| **Save / Apply** | Kaydet / Uygula | Kaydet ve uygula düğmeleri |

---

## 🚫 8. Çevrilmeyecek Kalıplar (Do Not Translate)

* **CLI Komutları:** `enable`, `disable`, `exit`, `end`, `write memory`, `reload`, `debug ...`
* **Port İsimleri:** `FastEthernet0/0`, `GigabitEthernet0/0/0`, `Serial0/1/0`, `Vlan1`
* **Dosya Uzantıları:** `.pkt`, `.pka`, `.pkz`, `.pts`, `.ptl`
* **Tescilli İsimler ve Kısaltmalar:** `Cisco`, `Packet Tracer`, `Easy VPN`, `Frame Relay`, `IOS`, `NVRAM`, `TFTP`, `FTP`, `SSH`, `Telnet`
* **Runtime Değişkenleri:** `[[variablename]]`, `[[query-type]]`, `[[Name]]`, `[[PORT]]`, `[[SIZE]]`, `%1`, `%2`, `%n`
