# 🎓 Öğrenci Görev Takip Sistemi

## 📌 Proje Hakkında

**Öğrenci Görev Takip Sistemi**, öğrencilerin derslerine ait ödev, proje ve sınav gibi görevlerini dijital ortamda düzenli bir şekilde takip edebilmelerini sağlayan web tabanlı bir uygulamadır.

Kullanıcılar sisteme kayıt olup giriş yaptıktan sonra:
- Derslerini ekleyebilir
- Derslere bağlı görevler oluşturabilir
- Görevlerin teslim tarihlerini takip edebilir
- Duyuruları görüntüleyebilir
- Görev ve duyurulara yorum yapabilir
- Görevlere dosya yükleyebilir

Amaç, öğrencilerin akademik süreçlerini daha düzenli, erişilebilir ve etkileşimli hale getirmektir.

---

## 🚀 Kullanılan Teknolojiler

- HTML5, CSS3, Bootstrap
- JavaScript
- ASP.NET Core MVC (veya PHP)
- SQL Server / MySQL
- Entity Framework Core

---

## 🗄️ Veritabanı Tasarımı

Projede toplam **8 tablo** bulunmaktadır:

### 👤 Users
Kullanıcı bilgilerini tutar.
- UserId
- FirstName
- LastName
- Email
- PasswordHash

---

### 📚 Courses
Kullanıcının derslerini içerir.
- CourseId
- UserId
- CourseName
- Lecturer
- Semester

---

### 📝 Tasks
Ödev, proje ve sınav görevleri.
- TaskId
- CourseId
- Title
- Description
- DueDate
- Priority
- Status

---

### 🏷️ Categories
Görev kategorileri.
- CategoryId
- CategoryName

---

### 🔔 Notifications
Kullanıcı bildirimleri.
- NotificationId
- UserId
- TaskId
- Message
- CreatedAt
- IsRead

---

### 📢 Announcements
Sistem duyuruları.
- AnnouncementId
- UserId
- Title
- Content
- CreatedAt

---

### 💬 Comments
Görev ve duyuru yorumları.
- CommentId
- UserId
- TaskId (nullable)
- AnnouncementId (nullable)
- CommentText
- CreatedAt

---

### 📁 Files
Görevlere yüklenen dosyalar.
- FileId
- TaskId
- UploadedByUserId
- FileName
- FilePath
- UploadedAt

---

## 🔗 İlişkiler

- Users → Courses (1-N)
- Courses → Tasks (1-N)
- Tasks → Files (1-N)
- Tasks → Comments (1-N)
- Users → Notifications (1-N)
- Users → Announcements (1-N)
- Users → Comments (1-N)
- Tasks ↔ Categories (opsiyonel ilişki)

---

## 📄 Proje Sayfaları

- Login / Register
- Dashboard
- Derslerim
- Görevlerim
- Görev Detay
- Kategoriler
- Bildirimler
- Duyurular
- Dosya Yükleme
- Profil Sayfası

---

## 🎯 Proje Kazanımları

Bu proje sayesinde:

- MVC mimarisi öğrenilir
- İlişkisel veritabanı tasarımı yapılır
- CRUD işlemleri geliştirilir
- Dosya yükleme sistemi oluşturulur
- Bildirim ve yorum sistemi kurulur
- Gerçek hayat senaryosuna yakın bir web uygulaması geliştirilir

---

## 📌 Lisans

Bu proje eğitim amaçlı geliştirilmiştir.
