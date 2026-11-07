# İki Asenkron Motorun Bağımsız Start-Stop Kumandası ve 3D Pano Tasarımı

**EPLAN Electric P8 | Elektrik Projelendirme | Klasik Kumanda | 3D Pano Tasarımı**

## 1. Proje Kapak Sayfası

![Proje Kapak Sayfası](01_Proje_Kapagi.png)

## 2. İçindekiler Dizini

![İçindekiler Dizini](02_Icindekiler_Dizini.png)

## 3. Proje Tanıtımı ve Teknik Bilgiler

Bu proje, iki adet üç fazlı asenkron motorun birbirinden bağımsız olarak çalıştırılması ve durdurulması amacıyla EPLAN Electric P8 kullanılarak hazırlanmıştır.

Proje kapsamında motor güç devreleri, 24 V DC kumanda devresi, koruma elemanları, kontaktörler, butonlar, sinyal lambaları ve 3D elektrik panosu tasarlanmıştır.

### Teknik Özellikler

| Özellik | Açıklama |
|---|---|
| Proje numarası | PRJ-001 |
| Proje sahibi | Mustafa Şahin |
| Yazılım | EPLAN Electric P8 |
| Proje türü | Elektrik Kumanda ve Pano Tasarımı |
| Motor sayısı | 2 |
| Motor gücü | 2 × 0,55 kW |
| Güç devresi gerilimi | 3~ 400 V AC |
| Kumanda devresi gerilimi | 24 V DC |
| Kontrol yöntemi | Klasik kontaktörlü kumanda |
| Motor koruması | Motor koruma şalteri |
| Proje ortamı | Eğitim / Simülasyon |

### Projenin Amacı

Bu çalışmanın amacı, endüstriyel elektrik otomasyon sistemlerinde kullanılan güç ve kumanda devrelerini uygulamalı olarak projelendirmek ve EPLAN üzerinden teknik dokümantasyon hazırlamaktır.

Proje ile aşağıdaki çalışmalar gerçekleştirilmiştir:

- Üç fazlı asenkron motor güç devrelerinin çizilmesi
- Motor koruma şalteri ve kontaktör bağlantılarının oluşturulması
- 24 V DC kumanda devresinin tasarlanması
- Start-Stop butonlarıyla bağımsız motor kontrolü
- Yardımcı kontaklarla mühürleme devresinin oluşturulması
- Çalıştırma ve durdurma sinyal lambalarının kullanılması
- Cihaz etiketleme ve çapraz referansların oluşturulması
- 3D pano yerleşim ve montaj tasarımı
- EPLAN proje raporlarının hazırlanması

## 4. İki Asenkron Motorun Güç Devresi

![İki Asenkron Motorun Güç Devresi](05_Motor_Guc_Devresi.png)

Güç devresinde iki adet 0,55 kW üç fazlı asenkron motor bulunmaktadır.

Her motor için ayrı koruma ve anahtarlama elemanları kullanılmıştır.

### Motor 1

- **-2F2:** Üç kutuplu otomatik sigorta
- **-2Q2:** Motor koruma şalteri
- **-4K1:** Motor güç kontaktörü
- **-2M2:** 0,55 kW üç fazlı asenkron motor

### Motor 2

- **-2F6:** Üç kutuplu otomatik sigorta
- **-2Q6:** Motor koruma şalteri
- **-4K6:** Motor güç kontaktörü
- **-2M6:** 0,55 kW üç fazlı asenkron motor

Motorlar birbirinden bağımsız olarak kontrol edilmektedir.

## 5. 230 V AC / 24 V DC Güç Kaynağı Devresi

![24 V DC Güç Kaynağı Devresi](06_DC_Guc_Kaynagi.png)

Kumanda sisteminin beslenmesi için 230 V AC girişli ve 24 V DC çıkışlı güç kaynağı kullanılmıştır.

### Kullanılan Ekipmanlar

- **-3G2:** AC/DC güç kaynağı
- **-3F2:** DC kumanda devresi koruma elemanı

Güç kaynağından elde edilen 24 V DC gerilim, kontaktör bobinlerinin ve sinyal lambalarının beslenmesinde kullanılmaktadır.

## 6. Start-Stop Kumanda Devresi

![Start-Stop Kumanda Devresi](07_Start_Stop_Kumanda_Devresi.png)

Kumanda devresi 24 V DC gerilimle çalışmaktadır.

İki motor için ayrı Start-Stop kontrol devreleri oluşturulmuştur.

### Motor 1 Çalışma Prensibi

1. **-4S1** yeşil Start butonuna basılır.
2. **-4K1** kontaktörü enerjilenir.
3. Kontaktörün ana kontakları kapanır ve motor çalışır.
4. K1 yardımcı NO kontağı üzerinden mühürleme sağlanır.
5. **-4P2** yeşil çalışma lambası yanar.
6. **-4S3** kırmızı Stop butonuna basıldığında **-4K3** durdurma kontaktörü enerjilenir.
7. K3'ün NC yardımcı kontağı açılır ve K1'in enerjisi kesilerek motor durdurulur.
8. **-4P4** kırmızı durdurma komutu lambası yanar.

### Motor 2 Çalışma Prensibi

Motor 2 aynı prensiple bağımsız olarak çalışmaktadır.

- **-4S6:** Yeşil Start butonu
- **-4K6:** Motor güç kontaktörü
- **-4P7:** Yeşil çalışma lambası
- **-4S8:** Kırmızı Stop butonu
- **-4K8:** Durdurma kontaktörü
- **-4P8:** Kırmızı durdurma komutu lambası

**Teknik Not:** Bu projede Start ve Stop butonlarının tamamı normalde açık (NO) kontaklıdır. Stop butonları durdurma kontaktörlerini enerjilendirir. Bu kontaktörlerin NC yardımcı kontakları üzerinden motor güç kontaktörlerinin enerjisi kesilir.

## 7. Yedek Besleme ve Klemens Bağlantıları

![Yedek Besleme ve Klemens Bağlantıları](08_Yedek_Besleme_Klemensleri.png)

Projede gelecekteki sistem genişletmelerinde kullanılabilecek yedek besleme çıkışları tasarlanmıştır.

### Yedek Bağlantılar

- **-5F1:** Üç fazlı yedek besleme koruması
- **-5F2:** 24 V DC yedek besleme koruması
- **-5X2:** Nötr bağlantı klemensi
- **-5X2.1:** Koruma topraklaması bağlantısı
- **-5X2.2:** DC dönüş hattı bağlantısı

Bu bağlantılar gelecekte sisteme ilave edilebilecek elektriksel ekipmanlar için ayrılmıştır.

## 8. 3D Pano Tasarımı ve Model Görünümleri

![3D Pano Tasarımı ve Model Görünümleri](04_3D_Pano_Model_Gorunumleri.png)

Projenin 3D pano yerleşimi EPLAN ortamında hazırlanmıştır.

### Pano Tasarımında Kullanılan Bileşenler

- Elektrik panosu gövdesi
- Montaj plakası
- DIN rayları
- Koruma elemanları
- Kontaktörler
- Klemens grupları
- Start-Stop butonları
- Sinyal lambaları

### Model Görünümleri

Pano tasarımının farklı açılardan incelenebilmesi için aşağıdaki model görünümleri oluşturulmuştur:

- KB İzometrik Görünüm
- Ön Görünüş
- KD İzometrik Görünüm

Bu görünümler, pano ekipmanlarının yerleşimini ve mekanik montaj düzenini göstermek amacıyla hazırlanmıştır.

## 9. Kullanılan Elektrik Ekipmanları

| Ekipman | Adet | Görevi |
|---|---:|---|
| Üç fazlı asenkron motor | 2 | Mekanik hareket oluşturmak |
| Motor koruma şalteri | 2 | Motor koruması |
| Motor güç kontaktörü | 2 | Motorun enerjisini açıp kapatmak |
| Durdurma kontaktörü | 2 | Durdurma komutunu işlemek |
| Yeşil NO Start butonu | 2 | Motor çalıştırma |
| Kırmızı NO Stop butonu | 2 | Motor durdurma komutu |
| Yeşil sinyal lambası | 2 | Çalıştırma durumunu göstermek |
| Kırmızı sinyal lambası | 2 | Durdurma komutunu göstermek |
| AC/DC güç kaynağı | 1 | 24 V DC kumanda beslemesi |
| Otomatik sigortalar | Projeye göre | Elektriksel koruma |
| Klemensler | Projeye göre | Elektriksel bağlantılar |

## 10. EPLAN Proje Dosyası

Projenin düzenlenebilir EPLAN yedeği `.zw1` formatında depoya eklenmiştir.

**Proje dosyası:**

`Iki Asenkron Motor Start Stop Kumanda ve Pano Tasarimi.zw1`

Proje yedeği, uyumlu EPLAN yazılımı ve uygun lisans ile geri yüklenerek incelenebilir.

### Kullanılan Yazılım

- EPLAN Electric P8
- EPLAN 3D Pano Yerleşimi
- EPLAN Proje Raporlama Araçları

### Önemli Açıklama

Bu çalışma eğitim ve kişisel portföy amacıyla hazırlanmıştır. Gerçek bir endüstriyel uygulamada kullanılmadan önce elektriksel güvenlik, koruma koordinasyonu, kablo kesitleri, ekipman uygunluğu ve ilgili standartlar açısından doğrulanması gerekmektedir.

---

## Proje Sahibi

**Mustafa Şahin**

**Elektrik Kumanda | Endüstriyel Otomasyon | EPLAN | PLC**

Bu proje, elektrik projelendirme ve endüstriyel otomasyon alanındaki teknik bilgi ve uygulama becerilerini geliştirmek amacıyla hazırlanmıştır.
