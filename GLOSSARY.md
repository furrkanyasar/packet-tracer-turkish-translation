# Cisco Packet Tracer - Ağ Terimleri ve Çeviri Standartları (Glossary)

Bu belge, Cisco Packet Tracer arayüzü, diyalogları ve yardım metinlerinde Türkçe dil tutarlılığını sağlamak için kullanılan standart terminoloji sözlüğüdür.

---

## 📌 Genel Çeviri Kuralları

1. **CLI Komutları ve Çıktıları ASLA Çevrilmez:**
   * Örnek: `show ip route`, `configure terminal`, `ping`, `traceroute`, `interface FastEthernet0/1`, `no shutdown`, `switchport mode access` doğrudan orijinal haliyle kalmalıdır.
2. **Protokol İsimleri ve Kısaltmaları:**
   * Protokol adları ve kısaltmaları (OSPF, EIGRP, BGP, RIP, STP, VLAN, Frame Relay, DHCP, DNS, NAT, ACL, ICMP, TCP, UDP vb.) orijinal haliyle korunur.
3. **Değişkenler ve Parametreler:**
   * `%1`, `%2`, `%n` gibi Qt değişkenleri değiştirilmez, sırası korunur.
   * Türkçedeki `%100`, `%50` gibi yüzdelik ifadelerin Qt tarafından değişken sanılmaması için `% 100` veya `%%100` formatında yazılır.
4. **Mnemonic (Kısayol) Karakterleri:**
   * `&File` -> `&Dosya`, `&Edit` -> `&Düzenle`, `&Options` -> `&Seçenekler`.

---

## 📖 Temel Ağ ve Arayüz Terimler Tablosu

| İngilizce Terim | Türkçe Karşılığı | Notlar / Örnek Kullanım |
|---|---|---|
| **Router** | Yönlendirici | Cihaz türü olarak |
| **Switch** | Anahtar | Cihaz türü olarak |
| **Hub** | Hub / Dağıtıcı | Hub olarak bırakılabilir |
| **Access Point (AP)** | Erişim Noktası | |
| **Default Gateway** | Varsayılan Ağ Geçidi | IP yapılandırma alanı |
| **Subnet Mask** | Alt Ağ Maskesi | IP yapılandırma alanı |
| **Routing / Routes** | Yönlendirme / Rotalar | "Yol" yerine "Rota" standardı |
| **Running Config** | Çalışan Yapılandırma | `Startup Config` (Başlangıç Yapılandırması) ile uyumlu |
| **Default Information Originate** | Varsayılan Bilgi Yayını (Default Information Originate) | OSPF varsayılan rota yayını |
| **Accounting (AAA)** | Muhasebe (Accounting) | "Hesaplama" değil; denetim ve kayıt tutma |
| **Frame Relay** | Frame Relay | Protokol adı korunur |
| **Hello / Beacon Interval** | Hello / Beacon Aralığı | Paket adı korunur ("Selam" vb. yapılmaz) |
| **Shared Secret** | Paylaşılan Gizli Parola (Shared Secret) | RADIUS / TACACS kimlik doğrulama |
| **Rack** | Kabin (Rack) | "Raf" yerine ağ sistem kabini |
| **Coverage Range** | Kapsama Menzili | Kablosuz ağ menzili |
| **Broadcast** | Yayın / Genel Yayın | |
| **Unicast** | Teke Gönderim (Unicast) | |
| **Multicast** | Çoka Gönderim (Multicast) | |
| **Packet** | Paket | |
| **Frame** | Çerçeve | Veri bağlantı katmanı birimi |
| **Payload** | Yük / Veri Yükü | |
| **Throughput** | İş Hacmi / Verim | |
| **Bandwidth** | Bant Genişliği | |
| **Delay / Latency** | Gecikme | |
| **Collision Domain** | Çarpışma Alanı | |
| **Broadcast Domain** | Yayın Alanı | |
| **Topology** | Topoloji | |
| **Workspace** | Çalışma Alanı | Logical/Physical Workspace |
| **Realtime Mode** | Gerçek Zamanlı Mod | |
| **Simulation Mode** | Simülasyon Modu | |
| **Event List** | Olay Listesi | Simülasyon paneli |
| **Activity Wizard** | Etkinlik Sihirbazı | |
| **Cluster** | Küme / Kümeleme | |
| **Inspect** | İncele | Büyüteç aracı |
| **Cable** | Kablo | Bağlantı türleri |
| **Straight-Through** | Düz Kablo | Bakır kablo türü |
| **Crossover** | Çapraz Kablo | Bakır kablo türü |
| **Fiber** | Fiber / Fiber Optik | |
| **Serial** | Seri | Seri kablo / Port |
| **Console** | Konsol | Konsol kablosu / Portu |
| **Port Forwarding** | Port Yönlendirme | |
| **Firewall** | Güvenlik Duvarı | |
| **Access Control List (ACL)** | Erişim Kontrol Listesi | |
| **Routing Table** | Yönlendirme Tablosu | |
| **MAC Address Table** | MAC Adres Tablosu | |
| **Neighbor** | Komşu | Yönlendirme protokollerinde |
| **Adjacency** | Bitişiklik / Komşuluk | OSPF vb. |
| **Metric** | Metrik | Yönlendirme maliyeti |
| **Hop Count** | Atlama Sayısı | RIP vb. |

---

## 🚫 Çevrilmemesi Gerekenler (Do Not Translate)

* **CLI Komutları:** `enable`, `disable`, `exit`, `end`, `write memory`, `reload`, `debug ...`
* **Port İsimleri:** `FastEthernet0/0`, `GigabitEthernet0/0/0`, `Serial0/1/0`, `Vlan1`
* **Dosya Uzantıları:** `.pkt`, `.pka`, `.pkz`, `.pts`, `.ptl`
* **Kalıplaşmış Kısaltmalar:** `PDU`, `CLI`, `GUI`, `IOS`, `NVRAM`, `RAM`, `ROM`, `TFTP`, `FTP`, `SSH`, `Telnet`, `Frame Relay`, `Easy VPN`
