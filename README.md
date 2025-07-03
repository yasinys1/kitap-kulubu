Kitap Kulübü Yönetim Sistemi
=============================

Bu proje, kitap okuma alışkanlığını desteklemek amacıyla geliştirilen bir topluluk yönetim sistemidir. Kullanıcılar kitap önerebilir, birbirleriyle mesajlaşabilir ve etkinliklere katılabilir. Yöneticiler (admin) kullanıcıları, kitapları ve etkinlikleri yönetebilir.

Kullanılan Teknolojiler
------------------------
- Next.js – App Router mimarisi
- Prisma ORM – Veritabanı yönetimi
- SQLite – Geliştirme ortamı için lokal veritabanı
- Tailwind CSS + Shadcn UI – Şık ve sade kullanıcı arayüzü

Kurulum Talimatları
--------------------
git clone https://github.com/yasinys1/kitap-kulubu
cd kitap-kulubu
npm install
npx prisma migrate dev --name init
npm run dev

diff
Her zaman ayrıntıları göster

Kopyala

.env dosyasına:
DATABASE_URL=\"file:./dev.db\"

Admin Giriş Bilgileri
----------------------
E-posta: admin@example.com  
Şifre: admin123

Temel Özellikler
----------------
- Kayıt Ol / Giriş Yap
- Profil Görüntüleme ve Güncelleme
- Rol Tabanlı Yetkilendirme (admin / user)
- Kullanıcılar arası mesajlaşma
- Kitap önerme & onay sistemi
- Etkinlik oluşturma & listeleme
- Admin paneli (kullanıcı/kitap/etkinlik kontrolü)
"""

report_text = """
Kitap Kulübü Yönetim Sistemi - Proje Raporu
===========================================

1. Proje Konusu ve Amacı
-------------------------
Kitap Kulübü Yönetim Sistemi, kullanıcıların kitap önerileri sunabileceği, etkinliklere katılabileceği ve diğer üyelerle etkileşime geçebileceği bir platformdur. Aynı zamanda yöneticilere kullanıcı ve içerik kontrolü sunar.

2. Planlama ve Geliştirme Süreci
--------------------------------
İlk olarak kullanıcı rolleri ve kimlik doğrulama mekanizması tasarlandı. Ardından her rolün sahip olacağı yetkiler belirlendi. UI bileşenleri Shadcn UI ile geliştirildi. Kodun her parçası modüler yazılarak sayfa/sunucu ayrımı net tutuldu.

3. Modüller ve İşlevleri
-------------------------
- Kullanıcı İşlemleri: Kayıt, giriş, çıkış, profil görüntüleme/güncelleme
- Rol Sistemi: Admin ve Normal kullanıcı rolleri
- Admin Paneli: Kullanıcı/kitap/etkinlik yönetimi
- Mesajlaşma: Kullanıcılar arası mesaj gönderimi
- Kitap Modülü: Önerilen kitaplar ve onay süreci
- Etkinlik Modülü: Admin tarafından düzenlenen etkinlik takibi

4. Kodlama Yapısı
------------------
- Next.js (App Router) mimarisi kullanıldı.
- Tüm veri yönetimi Prisma ORM ile kontrol ediliyor.
- Stil Tailwind CSS + Shadcn UI ile sağlandı.
- Kodlar bileşen tabanlı, okunabilir ve temiz yazıldı.

5. Kazanımlar ve Değerlendirme
-------------------------------
- Rol tabanlı erişim kontrolü oluşturmayı öğrendim.
- Gerçek veritabanı ilişkileri ve ORM mantığını kavradım.
- UI/UX tarafında modern arayüz geliştirmeyi deneyimledim.
- Tüm sistemi sıfırdan kurarak tam proje deneyimi kazandım.

6. Bileşenlerin Genel İşleyişi
------------------------------
- middleware.ts: Admin sayfalarına sadece admin erişimi sağlar.
- messages/page.tsx: Kullanıcılar arası etkileşim arayüzü.
- admin/books: Kitap onay arayüzü.
- admin/events: Etkinlik ekleme/silme işlemleri.
