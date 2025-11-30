# DİYABET TAKİP SİSTEMİ: Hasta ve Doktor Paneli

## 👥 Proje Sahipleri
* Ömer Faruk Toycu (@omertoycu)
* Ali Berke Erenler (@aliberkerenler)

---

## 🎯 Proje Amacı
Bu proje, diyabet hastalarının günlük sağlık verilerini (kan şekeri, insülin dozu, diyet, egzersiz) düzenli olarak takip etmelerini ve bu verileri doktorlarıyla paylaşmalarını sağlayan, Python tabanlı bir masaüstü uygulamasıdır. Sistem, **Hasta** ve **Doktor** olmak üzere iki farklı kullanıcı paneli sunarak diyabet yönetimini kolaylaştırmayı hedefler.

## 🛠️ Teknolojiler ve Kütüphaneler
* **Dil:** Python
* **Arayüz (UI):** Masaüstü Grafik Kullanıcı Arayüzü (GUI) (Tarafında belirtilen modüllerden anlaşılmaktadır)
* **Veritabanı:** SQLite (İlişkisel veritabanı, `db_connection.py` ve `schema.sql` dosyalarından çıkarılmıştır)
* **Veritabanı Şeması:** `schema.sql` dosyası ile verilerin depolanma yapısı tanımlanmıştır.

---

## 🏗️ Mimari ve Modüller
Sistem, kullanıcı rolüne ve takip edilen veri türüne göre modüler bir yapıdadır:

### 1. Kullanıcı Panelleri
* **`login_page.py`:** Kullanıcıların (Hasta/Doktor) kimlik doğrulaması yaparak sisteme giriş yapmasını sağlar.
* **`patient_panel.py`:** Hastaların kendi sağlık verilerini (kan şekeri, insülin vb.) girebildiği ve görüntüleyebildiği ana paneldir.
* **`doctor_panel.py`:** Doktorların, takip ettikleri hastaların detaylı verilerini görebildiği, analiz edebildiği ve tedavi kararları alabileceği paneldir.

### 2. Takip Modülleri (Veri Giriş Sayfaları)
* **`blood_sugar_page.py`:** Hastanın kan şekeri ölçümlerini kaydettiği arayüz.
* **`insulin_page.py`:** Kullanılan insülin dozlarını ve zamanlarını kaydettiği arayüz.
* **`diet_page.py`:** Tüketilen yiyecek ve diyet bilgilerini kaydettiği arayüz.
* **`exercise_page.py`:** Yapılan fiziksel aktivitelerin süresini ve yoğunluğunu kaydettiği arayüz.
* **`symptom_page.py`:** Yaşanan özel semptomları (belirtileri) kaydetmek için kullanılır.
* **`statistics_page.py`:** Kaydedilen verilere dayanarak istatistiksel analizler ve grafiksel özetler sunar.

---

## 🚀 Çalıştırma Talimatları
1.  **Gereklilikleri Kurun:** Projenin çalışması için gerekli tüm Python kütüphanelerini kurun.
2.  **Veritabanını Hazırlayın:** Veritabanı bağlantısını (`db_connection.py`) ayarlayın ve veritabanı şemasını (`schema.sql`) kullanarak tablo yapısını oluşturun.
3.  **Uygulamayı Başlatın:** Projenin ana dosyası olan `main.py` dosyasını çalıştırın.
4.  Açılan giriş ekranından Hasta veya Doktor rolü ile sisteme giriş yaparak ilgili panellere erişim sağlayın.
