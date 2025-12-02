
# Wine Quality Analysis & Prediction

Bu projede, şarapların kimyasal özellikleri ile kaliteleri arasındaki ilişki analiz edilmiştir.

[Analize Google Colab üzerinden erişmek için tıklayınız](https://colab.research.google.com/drive/1Bnmknj6TvorbPOiC__A7xH_T8Gx23Bzt)

---

## Proje Özeti ve Amaç
Şarap kalitesi subjektif tadım testlerine dayanıyor gibi görünse de, aslında kimyasal dengelerin fiziksel bir sonucudur. Bu projede UCI Machine Learning Repository'den alınan veri seti kullanılarak:
* Kaliteyi doğrudan artıran ve azaltan bileşenler tespit edilmiş,
* Değişkenler arasındaki gizli ilişkiler incelenmiş,
* Şaraplar kalite sınıflarına ayrılarak kritik farklar görselleştirilmiştir.

## Veri Seti Hakkında
Analiz, Portekiz'in "Vinho Verde" şaraplarına ait verileri içerir.
* Gözlem Sayısı: 1143
* Özellik Sayısı: 13
* Veri Durumu: Eksik (Null) veya tekrarlayan veri bulunmamaktadır.

| Özellik | Açıklama |
| :--- | :--- |
| **Fixed Acidity** | Şaraptaki tartarik asit miktarı (Şarabın temel yapısını oluşturur). |
| **Volatile Acidity** | Şaraptaki asetik asit miktarı (Yüksekse sirkeleşmeye neden olur). |
| **Citric Acid** | Tazelik katan asit türü (Koruyucu etki). |
| **Residual Sugar** | Fermantasyon sonrası kalan şeker. |
| **Chlorides** | Şaraptaki tuz miktarı. |
| **Free Sulfur Dioxide** | Mikrobiyal bozulmayı önleyen serbest sülfür formu. |
| **Total Sulfur Dioxide** | Serbest ve bağlı sülfür dioksit miktarı. |
| **Density** | Şarabın yoğunluğu (Alkol ve asit oranına göre değişir). |
| **pH** | Asitlik derecesi (0-14 arası). |
| **Sulphates** | Sülfür dioksit seviyesini koruyan katkı maddesi. |
| **Alcohol** | Şarabın alkol yüzdesi (Kalite üzerindeki en güçlü etken). |
| **Quality** | Hedef değişken (0-10 arası puan). |

---

## Temel Bulgular ve Analiz Sonuçları

Yapılan istatistiksel analizler ve görselleştirmeler sonucunda aşağıdaki kritik bulgulara ulaşılmıştır:

### 1. Kaliteyi Belirleyen Faktörler (Korelasyon Analizi)
* Alkol (+0.48): Kalite ile en güçlü pozitif ilişkiye sahiptir. Alkol oranı arttıkça kalite puanı belirgin şekilde artmaktadır.
* Uçucu Asitlik (-0.41): Kalite üzerindeki en güçlü negatif etkidir. "Sirkeleşme" belirtisi olduğu için kaliteli şaraplarda minimum seviyededir.
* Sülfatlar (+0.26) & Sitrik Asit (+0.24): Kaliteyi destekleyen ikincil faktörlerdir.

### 2. Fiziksel ve Kimyasal İlişkiler
* Asitlik & pH: Beklendiği üzere, asit miktarı (Fixed Acidity) arttıkça pH değeri düşmektedir (Güçlü Ters Orantı).
* Yoğunluk (Density) Paradoksu: Yoğunluk kaliteyi doğrudan etkilemez. Ancak Alkol sudan hafif olduğu için, yüksek alkollü (kaliteli) şarapların yoğunluğu fiziksel bir sonuç olarak düşük çıkmaktadır.

---

## Kaliteli Şarabın Formülü (Sonuç)

Veri setindeki şaraplar Düşük, Orta ve Yüksek kalite olarak gruplandırıldığında, mükemmel şarap ile sıradan şarap arasındaki fark netleşmiştir:

**Analiz Sonucu:**
Kaliteli bir şarap üretmek için gereken kimyasal imza şudur:
* %11.5 ve üzeri Alkol
* Yüksek Sitrik Asit ve Sülfat
* Minimum Uçucu Asit (Volatile Acidity)

![Grafik Açıklaması](dagılımlar.png)

---

## Kullanılan Teknolojiler
* Python 3.x
* Pandas & NumPy
* Seaborn & Matplotlib


*Bu proje Veri Bilimi portfolyo çalışması olarak hazırlanmıştır.*
