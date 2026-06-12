╔══════════════════════════════════════════════════════════════════╗
║           OKUL YÖNETİM SİSTEMİ — KULLANIM KILAVUZU              ║
║                     (Sürüm 1.0)                                  ║
╚══════════════════════════════════════════════════════════════════╝

Bu uygulama; öğrenci, öğretmen ve yönetici rollerine sahip üç
katmanlı bir okul yönetim sistemidir. Ders kaydı, not takibi,
devamsızlık yönetimi, sınav takvimi ve bildirim gönderimi gibi
temel okul işlemlerini masaüstü arayüz üzerinden yönetmenizi sağlar.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    1. SİSTEM GEREKSİNİMLERİ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  - İşletim Sistemi : Windows 7 / 8 / 10 / 11
  - .NET Framework  : 4.7.2 veya üzeri
  - Microsoft Access Database Engine (ACE OleDB sürücüsü)
    → Yüklü değilse aşağıdaki adresten indirin:
      https://www.microsoft.com/en-us/download/details.aspx?id=54920
    → 64-bit Windows kullanıyorsanız 64-bit sürümünü tercih edin.

  NOT: Microsoft Office kurulu bilgisayarlarda ACE sürücüsü
  genellikle zaten yüklüdür.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                       2. KURULUM VE ÇALIŞTIRMA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  1. ZIP dosyasını bir klasöre çıkarın.

  2. Aşağıdaki klasör yapısının eksiksiz bulunduğunu kontrol edin:

       OkulYonetimSistemi/
       ├── OkulYonetimSistemi.exe      ← Çalıştırılacak uygulama
       ├── 42496school_99040.ico       ← Uygulama ikonu
       └── Database/
           └── OkulDb.accdb            ← Veritabanı dosyası

  3. OkulYonetimSistemi.exe dosyasını çift tıklayarak uygulamayı
     başlatın.

  ÖNEMLİ: "Database" klasörü ve içindeki "OkulDb.accdb" dosyası,
  .exe ile aynı dizinde bulunmak ZORUNDADIR. Aksi takdirde uygulama
  "Veritabanı bulunamadı!" uyarısı verir ve çalışmaz.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                     3. GİRİŞ EKRANI
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Uygulama açıldığında üç sekme içeren bir giriş ekranı gelir:
  "Yönetici", "Öğretmen" ve "Öğrenci".

  Giriş yapmak için:
    → Uygun sekmeyi seçin.
    → TC Kimlik Numaranızı girin (11 hane, son hane çift sayı).
    → Şifrenizi girin.
    → "Giriş" butonuna tıklayın.

  TC KİMLİK NO KURALI:
  Sistem, TC kimlik numarasının son hanesinin çift (0, 2, 4, 6, 8)
  olmasını zorunlu kılar. Yanlış biçimde girilirse uyarı verilir.

  ─── VARSAYILAN TEST GİRİŞ BİLGİLERİ ─────────────────────────

  Rol          | TC Kimlik No   | Şifre
  -------------|----------------|------
  Yönetici     | 30000000002    | 1234
  Öğretmen     | 10000000002    | 1234
  Öğrenci      | 20000000002    | 1234

  (Diğer örnek öğretmenler: 10000000004, 10000000006 — Şifre: 1234)
  (Diğer örnek öğrenciler : 20000000004, 20000000006 — Şifre: 1234)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               4. YÖNETİCİ PANELİ (Admin)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Sol kenar çubuğunda beş bölüm bulunur:

  ┌──────────────────────────────────────────────────────────────┐
  │ 📚 Ders Kaydı                                                │
  │   - Sisteme yeni ders ekleyin.                               │
  │   - Derse sorumlu öğretmen atayın.                           │
  │   - Mevcut dersleri listeleyin ve silin.                     │
  ├──────────────────────────────────────────────────────────────┤
  │ 📅 Ders Programı                                             │
  │   - Sınıf, ders, öğretmen, gün ve saat bilgilerini girerek  │
  │     haftalık ders programı oluşturun.                        │
  │   - Var olan program girişlerini silebilirsiniz.             │
  ├──────────────────────────────────────────────────────────────┤
  │ 🎓 Öğrenci Kaydı                                            │
  │   - Yeni öğrenci ekleyin (Ad-Soyad, TC, Şifre, Sınıf).     │
  │   - Mevcut öğrencileri görüntüleyin ve silin.               │
  ├──────────────────────────────────────────────────────────────┤
  │ 📋 Devamsızlık                                               │
  │   - Öğrencilerin derse göre devamsızlık bilgilerini          │
  │     görüntüleyin ve güncelleyin.                             │
  │   - Özürsüz gün sayısını ayrıca takip edin.                 │
  ├──────────────────────────────────────────────────────────────┤
  │ 🔔 Bildirim Gönder                                           │
  │   - Tüm sınıflara veya belirli bir sınıfa bildirim gönderin.│
  │   - Başlık ve mesaj alanlarını doldurup "Gönder" deyin.     │
  └──────────────────────────────────────────────────────────────┘

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               5. ÖĞRETMEN PANELİ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Sol kenar çubuğunda altı bölüm bulunur:

  ┌──────────────────────────────────────────────────────────────┐
  │ 📅 Ders Programım                                            │
  │   - Yalnızca kendi derslerinizin haftalık programını         │
  │     görüntüler.                                              │
  ├──────────────────────────────────────────────────────────────┤
  │ 👥 Öğrencilerim                                              │
  │   - Verdiğiniz derse göre öğrencileri filtreleyin.          │
  │   - Her öğrencinin not ve devamsızlık durumunu görün.       │
  ├──────────────────────────────────────────────────────────────┤
  │ 📋 Devamsızlık                                               │
  │   - Öğrencilerin devamsızlık ve özürsüz gün sayılarını      │
  │     güncelleyin.                                             │
  ├──────────────────────────────────────────────────────────────┤
  │ 📝 Sınav Ekle                                                │
  │   - Sınav adı, tarih, saat ve açıklama girerek sınav        │
  │     takvime ekleyin.                                         │
  │   - Hangi sınıf ve derse ait olduğunu belirtin.             │
  ├──────────────────────────────────────────────────────────────┤
  │ ✏️  Not Güncelle                                             │
  │   - Öğrencilerin vize ve final notlarını girin/güncelleyin. │
  │   - Hesaplanan ortalama (vize %40 + final %60) otomatik     │
  │     gösterilir.                                              │
  ├──────────────────────────────────────────────────────────────┤
  │ 🔔 Bildirim Gönder                                           │
  │   - Belirli bir sınıfa veya tüm sınıflara duyuru gönderin. │
  └──────────────────────────────────────────────────────────────┘

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               6. ÖĞRENCİ PANELİ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Sol kenar çubuğunda dört bölüm bulunur:

  ┌──────────────────────────────────────────────────────────────┐
  │ 📅 Ders Programım                                            │
  │   - Bulunduğunuz sınıfın haftalık ders programını görün.    │
  ├──────────────────────────────────────────────────────────────┤
  │ 📊 Notlarım                                                  │
  │   - Her derse ait vize, final ve hesaplanmış ortalamanızı   │
  │     görüntüleyin.                                            │
  │   - Geçme/kalma durumunuzu (50 ve üzeri = geçer) takip edin.│
  ├──────────────────────────────────────────────────────────────┤
  │ 📆 Sınav Takvimi                                             │
  │   - Sınıfınıza ait yaklaşan sınavların tarih ve saatlerini  │
  │     görün.                                                   │
  ├──────────────────────────────────────────────────────────────┤
  │ 🔔 Bildirimler                                               │
  │   - Öğretmen ve yöneticiden gelen duyuruları okuyun.        │
  └──────────────────────────────────────────────────────────────┘

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               7. VERİTABANI YAPISI
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Uygulama, Microsoft Access formatında (.accdb) yerel bir
  veritabanı kullanır. Veritabanı dosyası:
    → exe ile aynı dizindeki "Database/OkulDb.accdb" konumundadır.

  Tablolar ve içerikleri:

    Siniflar        : Sınıf adları (9/A, 9/B, 10/A ... 12/B)
    Ogretmenler     : Öğretmen bilgileri ve giriş kimlik bilgileri
    Ogrenciler      : Öğrenci bilgileri, sınıf ataması
    Adminler        : Yönetici hesapları
    Dersler         : Ders adları ve sorumlu öğretmen
    DersProgrami    : Haftalık ders çizelgesi (gün + saat)
    Kayitlar        : Öğrenci bazlı not ve devamsızlık kayıtları
    SinavTakvimi    : Sınav tarih, saat ve açıklama bilgileri
    Bildirimler     : Öğretmen/yönetici tarafından gönderilen duyurular

  Veritabanına doğrudan erişmek için Microsoft Access veya
  herhangi bir ACCDB uyumlu veritabanı yöneticisi kullanabilirsiniz.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               8. SIK KARŞILAŞILAN SORUNLAR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  SORUN  : "Veritabanı bulunamadı!" uyarısı çıkıyor.
  ÇÖZÜM  : OkulDb.accdb dosyasının "Database" klasörüne yerleştirildiğinden
            ve klasörün .exe ile aynı dizinde olduğundan emin olun.

  SORUN  : Uygulama açılmıyor veya hata veriyor.
  ÇÖZÜM  : Microsoft ACE OleDB sürücüsünün kurulu olduğunu kontrol edin.
            (Bkz. Bölüm 1 — Sistem Gereksinimleri)

  SORUN  : Giriş yapılamıyor, "Hatalı TC veya şifre!" diyor.
  ÇÖZÜM  : Doğru sekmeyi (Yönetici / Öğretmen / Öğrenci) seçtiğinizden
            ve TC numarasını tam 11 hane girdiğinizden emin olun.

  SORUN  : TC kimlik no alanına harf giriliyor / kabul edilmiyor.
  ÇÖZÜM  : Bu alan yalnızca rakam kabul eder ve son hane çift olmalıdır.
            Örnek geçerli TC: 10000000002

  SORUN  : Not hesabı yanlış görünüyor.
  ÇÖZÜM  : Sistem vize notunu %40, final notunu %60 oranında ağırlıklandırır.
            Ortalama = (Vize × 0.4) + (Final × 0.6)
            50 ve üzeri geçer kabul edilir.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               9. YEDEKLİ ÇALIŞMA (ÖNERİ)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Tüm veriler OkulDb.accdb dosyasında tutulur. Düzenli aralıklarla
  bu dosyayı kopyalayarak yedek almanız önerilir. Dosya bozulursa
  tüm kayıtlar kaybedilebilir.

  Yedek almak için: Database/OkulDb.accdb dosyasını farklı bir
  konuma kopyalamanız yeterlidir.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
               10. TEKNİK BİLGİ (GELİŞTİRİCİLER İÇİN)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Platform    : C# Windows Forms (.NET Framework 4.7.2)
  Veritabanı  : Microsoft Access (.accdb) — OleDB bağlantısı
  IDE         : Visual Studio (Solution: OkulYonetimSistemi.sln)
  Mimari      : 3 katman — Forms (UI), DAL (DbHelper / DatabaseSetup),
                Models (Theme)

  Proje klasör yapısı:
    Forms/          → LoginForm, AdminForm, OgretmenForm, OgrenciForm
    DAL/            → DbHelper.cs (sorgu yardımcısı),
                       DatabaseSetup.cs (tablo oluşturucu)
    Models/         → Theme.cs (renk ve font sabitleri)
    Database/       → OkulDb.accdb (veritabanı)

  Kaynak kodu derlemek için Visual Studio 2019 veya üzerini
  açıp OkulYonetimSistemi.sln dosyasını yükleyin ve Build > Build
  Solution (Ctrl+Shift+B) komutunu çalıştırın.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
