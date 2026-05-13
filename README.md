# MedBridge

**Kronik Hastalık Öz Takip ve Uzaktan Sağlık Paylaşım Paneli**

MedBridge, diyabet (şeker) ve hipertansiyon (tansiyon) gibi düzenli ölçüm ve sıkı takip gerektiren kronik rahatsızlıklara sahip bireylerin günlük sağlık verilerini kayıt altına aldığı ve bu verileri hekimleriyle kolay, güvenli ve yapılandırılmış bir şekilde paylaşabildiği dijital bir sağlık köprüsüdür.

## Proje Odak Noktaları ve İşleyiş

Sistem, hastanın kendi sağlık durumunu izlemesini (self-tracking) basitleştirirken, doktorların da doğru teşhis ve tedavi kararları alabilmesi için ihtiyaç duyduğu veri setlerini sunar:

*   **Düzenli Veri Kaydı ve Analizi:** Kullanıcılar kan şekeri, kan basıncı (tansiyon), nabız ve kilo gibi günlük ölçümlerini sisteme girer. Sistem bu verileri zaman serisi (time-series) grafiklerine dönüştürerek hastanın genel sağlık eğilimini ortaya koyar.
*   **Hekimle Güvenli Köprü:** Hasta, dilediği tarih aralığındaki ölçümlerini platform üzerinden doktoruna özel, tek kullanımlık bir erişim kodu veya güvenli bir bağlantı ile açabilir. Doktor, verileri MedBridge hekim paneli üzerinden detaylıca inceleyebilir veya dışa aktarabilir.
*   **Akıllı Eşik Uyarıları:** Girilen sağlık verileri belirlenen tıbbi risk sınırlarının (hipoglisemi, hipertansiyon krizi vb.) dışında kalıyorsa, sistem anında hastaya önleyici uyarılar verir. Hastanın onayına bağlı olarak, doktorun sistemine de "riskli durum" bildirimi iletilebilir.
*   **Kapsamlı Sağlık Günlüğü:** Sadece sayısal ölçümler değil; beslenme detayları, ruh hali ve hissedilen semptomlar da sisteme not edilerek doktorun daha bütüncül bir değerlendirme yapması sağlanır.

## Mimari Yaklaşım ve Teknoloji Yığını

*   **Frontend (Hasta Mobil Uygulaması):** React Native veya Flutter. Özellikle ileri yaş grubundaki hastaların zorlanmadan kullanabilmesi için yüksek erişilebilirlik (accessibility) standartlarına sahip, sade ve büyük butonlu bir mobil arayüz.
*   **Frontend (Hekim Web Paneli):** React.js veya Next.js. Doktorların poliklinik ortamında masaüstü bilgisayarlarından detaylı hasta grafiklerini ve verilerini analiz edebileceği profesyonel web paneli.
*   **Backend (API ve İş Mantığı):** Node.js (NestJS) veya Python (FastAPI). Verilerin alınması, hekim-hasta yetkilendirmelerinin (Authorization) yapılması ve raporların oluşturulması için güvenli REST veya GraphQL mimarisi.
*   **Veritabanı ve Güvenlik:** PostgreSQL (İlişkisel hasta-hekim ağacını kurmak için). Sağlık verileri kritik kişisel veri (KVKK / HIPAA) kapsamında olduğu için, veri tabanı seviyesinde şifreleme (Data-at-rest encryption) ve erişim loglaması (Audit logging) mutlaka uygulanır.
*   **Veri Görselleştirme (Grafikler):** Hekim paneli ve mobil uygulama içi eğilim çizimleri için D3.js, Chart.js veya Recharts.

---
