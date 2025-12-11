# 🦷 DişHane - Tam Kapsamlı Klinik Yönetim Yazılımı (Full-Stack Bitirme Projesi)

Bu proje, **Yazılım Mühendisliği Lisans Eğitimimin Bitirme Projesi** olarak sıfırdan geliştirilmiştir. Bir Diş Kliniği veya Polikliniğin tüm idari ve tıbbi iş akışlarını dijitalleştirmek amacıyla tasarlanmış, **MVC (Model-View-Controller) mimarisi** üzerine kurulu, özelleştirilmiş bir **Klinik Yönetim Sistemi** yazılımıdır.

Sistem; **çoklu kullanıcı yetkilendirmesi, karmaşık veri modelleme** ve **sunucu tarafı iş mantığı** konularındaki mühendislik yetkinliğimi göstermektedir.

## 🔗 Proje Bilgileri
- **Proje Tipi:** Full-Stack Web Uygulaması
- **Mimari Desen:** Özelleştirilmiş PHP MVC
- **Backend Dili:** PHP 
- **Veritabanı:** MySQL
- **Canlı Demo:** Bu proje sunucu tarafı (PHP/MySQL) gerektirdiği için genel kullanıma açık canlı demosu bulunmamaktadır. Yerel kurulum adımları aşağıdadır.

---

## ✨ Ana Özellikler ve Geliştirme Alanları

Projenin temel gücü, bir kliniğin karmaşık iş süreçlerini yönetme yeteneğidir:

### 1. Sistem Mimarisi ve Backend (PHP / MySQL)

* **MVC Mimarisi Uygulaması:** Kodun Veritabanı, İş Mantığı ve Sunum katmanlarına (Model, Controller, View) ayrılması ile projenin ölçeklenebilirliği sağlanmıştır.
* **Veritabanı Modelleme:** Randevu, Teşhis, Envanter gibi ilişkisel verilerin yönetimi için özelleştirilmiş Model sınıfları geliştirilmiştir.
* **Merkezi Rota Yönetimi:** Temiz URL yapısı ve yönlendirme sistemi (`routes/web.php`) kullanılarak uygulama navigasyonu kontrol altına alınmıştır.

### 2. Gelişmiş Kullanıcı ve Yetkilendirme Yönetimi

Sistem, kliniğin hiyerarşik yapısını yansıtan dört farklı kullanıcı rolüne özel paneller sunar:

| Kullanıcı Rolü | Temel Modüller ve Yetkiler | İlgili Dizin Kanıtı |
| :--- | :--- | :--- |
| **Admin** | Personel Yönetimi, Klinik İstatistikleri. | `views/dashboard/admin/` |
| **Doktor** | Randevu Takibi, Hastalara Teşhis Girişi (`Diagnosis`), Malzeme Kullanımı Kaydı. | `views/dashboard/doktor/` |
| **Sekreter** | Randevu Oluşturma/Yönetme, Stok/Envanter Takibi, Tıbbi Kayıtları Görüntüleme. | `views/dashboard/sekreter/` |
| **Hasta** | Kendi Randevularını Planlama, Tıbbi Geçmişini İnceleme. | `views/dashboard/hasta/` |

### 3. Ön Yüz ve Kullanıcı Deneyimi (Front-End)

* **Duyarlı Panel Tasarımı:** Tüm yönetim panelleri (Dashboard), farklı ekran boyutlarında kullanılabilirlik sağlamak üzere duyarlı (responsive) olarak tasarlanmıştır.
* **Veri Odaklı Arayüz:** Kullanıcıların karmaşık verileri (Randevu listeleri, Envanter tablosu) kolayca okuyup yönetebileceği sade ve işlevsel bir arayüz geliştirilmiştir.
* **Ajax Kullanımı:** Kullanıcı arayüzünde dinamik veri alışverişi için Ajax teknolojisi kullanılarak sayfa yenileme ihtiyacı en aza indirilmiştir.

## 🛠️ Kullanılan Teknolojiler

| Kategori | Teknolojiler | Kullanım Amacı |
| :--- | :--- | :--- |
| **Backend Dili** | **PHP** | Tüm sunucu tarafı iş mantığı ve veritabanı etkileşimi. |
| **Veritabanı** | **MySQL** | İlişkisel verilerin depolanması ve yönetimi. |
| **Mimari Desen** | **MVC** | Kod organizasyonu ve sürdürülebilirlik. |
| **Front-End** | **HTML5, CSS3, JavaScript, Ajax** | Kullanıcı arayüzü ve dinamik veri alışverişi. |

---

## 💻 Projeyi Yerel Ortamda Çalıştırma Kılavuzu (XAMPP Gerekli)

1.  **Depoyu Klonlayın:**
    ```bash
    git clone [https://github.com/sena-nur-ozdemir/DisHane)
    ```
2.  **Dosyaları Taşıyın:** İndirilen `DisHane` klasörünü XAMPP kurulumunuzdaki **`htdocs`** klasörünün içine taşıyın.
3.  **Veritabanı Kurulumu:**
    * XAMPP Control Panel'i açın ve **Apache** ile **MySQL** servislerini başlatın.
    * Tarayıcınızda `http://localhost/phpmyadmin` adresine gidin ve yeni bir veritabanı oluşturun (Örn: `dishane_db`).
    * **"İçe Aktar (Import)"** sekmesine gidin ve deponun ana dizininde bulunan **`dishane_db.sql`** dosyasını bu yeni veritabanına yükleyin.
4.  **Veritabanı Bağlantısını Yapılandırın:**
    * **`config/Database.php`** dosyasını açın.
    * İçindeki veritabanı bağlantı bilgilerini (DB adı, kullanıcı adı, şifre) yerel XAMPP ayarlarınıza göre güncelleyin.
5.  **Uygulamayı Başlatın:** Tarayıcınızda şu adrese gidin:
    ```
    http://localhost/DisHane/public
    ```
---

## 📸 Proje Fotoğrafları 

### 🔐 Giriş Sayfası

<img width="1917" height="970" alt="dishanefoto18" src="https://github.com/user-attachments/assets/21a26256-dd43-4bdc-a375-16bcabc6d4c0" />

### 🔐 Admin Paneli 

<img width="1918" height="966" alt="dishanefoto14" src="https://github.com/user-attachments/assets/ea38298e-4576-48e9-b864-29c9194ecd38" />

### 🔐 Admin Paneli Klinik İstatistikleri
<img width="1916" height="967" alt="dishanefoto15" src="https://github.com/user-attachments/assets/8ba220c0-b8a3-44ad-92d2-fb6c188a52a8" />

<img width="1918" height="953" alt="dishanefoto16" src="https://github.com/user-attachments/assets/033f0d09-74b5-4a4d-94a3-35f4f643c3fa" />

### 🔐 Admin Paneli Personel İşlemleri

<img width="1918" height="968" alt="dishanefoto17" src="https://github.com/user-attachments/assets/49737674-cc42-4e80-b50e-c580327c469b" />

### 👩‍⚕️ Doktor Paneli

<img width="1918" height="967" alt="dishanefoto1" src="https://github.com/user-attachments/assets/24761fd4-e673-4720-9940-68697ada34f6" />

### 📅 Doktor Paneli Randevu Takvimi

<img width="1918" height="970" alt="dishanefoto2" src="https://github.com/user-attachments/assets/563e9f18-0131-4f1b-b216-09494ce6194a" />

### 📦 Doktor Paneli Malzeme Kullanımı

<img width="1918" height="957" alt="dishanefoto3" src="https://github.com/user-attachments/assets/70a566b1-5234-4ec4-8600-4167befa516c" />

### 🧾 Doktor Paneli Tıbbi Kayıtlar

<img width="1917" height="967" alt="dishanefoto4" src="https://github.com/user-attachments/assets/f95ba020-524a-4274-823e-203a2c74f360" />

### 🗂️ Sekreter Paneli

<img width="1918" height="913" alt="dishanefoto5" src="https://github.com/user-attachments/assets/875d451b-b745-4609-bb18-b5abc22f5372" />

### 📅 Sekreter Paneli Doktor Çalışma Saatleri Oluşturma Sayfası

<img width="1918" height="966" alt="dishanefoto7" src="https://github.com/user-attachments/assets/d66fba95-e9e9-4a71-a0e4-5f754241a400" />

### 📦 Sekreter Paneli Stok Yönetimi

<img width="1913" height="968" alt="dishanefoto9" src="https://github.com/user-attachments/assets/1e0861e7-d1dd-43d3-82dc-514e3b0e267f" />

<img width="1918" height="972" alt="dishanefoto10" src="https://github.com/user-attachments/assets/b00497fc-04ae-4a3a-9a28-90978aaa252d" />

### 📅 Sekreter Paneli Randevu Görüntüleme

<img width="1917" height="968" alt="dishanefoto8" src="https://github.com/user-attachments/assets/ae8ecfc0-d801-4971-bc43-d5acb9c29e09" />

### 🧾 Hasta Paneli

<img width="1917" height="967" alt="dishanefoto12" src="https://github.com/user-attachments/assets/70afbbf3-4d95-489f-a6ac-3dfcd862edcb" />

### 📋 Hasta Paneli Randevu Oluşturma

<img width="1918" height="966" alt="dishanefoto13" src="https://github.com/user-attachments/assets/cf84ec60-a3db-4794-af4d-c28034eab66a" />

---
## Geliştirici
- **Sena Nur Özdemir** – [GitHub](https://github.com/sena-nur-ozdemir)
