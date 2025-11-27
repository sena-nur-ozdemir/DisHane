# 🦷 DişHane - Tam Kapsamlı Klinik Yönetim Yazılımı (Full-Stack Bitirme Projesi)

Bu proje, **Yazılım Mühendisliği Lisans Eğitimimin Bitirme Projesi** olarak sıfırdan geliştirilmiştir. Bir Diş Kliniği veya Polikliniğin tüm idari ve tıbbi iş akışlarını dijitalleştirmek amacıyla tasarlanmış, **MVC (Model-View-Controller) mimarisi** üzerine kurulu, özelleştirilmiş bir **Klinik Yönetim Sistemi** yazılımıdır.

**çoklu kullanıcı yetkilendirmesi, karmaşık veri modelleme** ve **sunucu tarafı iş mantığı** konusundaki yetkinliğimi kanıtlamaktadır.

## 🔗 Proje Bilgileri
> **Proje Tipi:** Full-Stack Web Uygulaması
> **Mimari Desen:** Özelleştirilmiş PHP MVC
> **Backend Dili:** PHP 
> **Veritabanı:** MySQL
> **Canlı Demo:** Bu proje sunucu tarafı (PHP/MySQL) gerektirdiği için genel kullanıma açık canlı demosu bulunmamaktadır. Yerel kurulum adımları aşağıdadır.

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
    git clone [https://github.com/senathecoder/DisHane](https://github.com/senathecoder/DisHane)
    ```
2.  **Dosyaları Taşıyın:** İndirilen `DişHane` klasörünü XAMPP kurulumunuzdaki **`htdocs`** klasörünün içine taşıyın.
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

## Geliştirici
- **Sena Nur Özdemir** – [GitHub](https://github.com/senathecoder)
