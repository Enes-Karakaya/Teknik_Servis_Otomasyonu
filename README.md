# Teknik Servis Otomasyonu

Bu proje, C# programlama dili kullanılarak geliştirilmiş bir teknik servis otomasyon sistemidir. Teknik servis firmalarının müşteri taleplerini, arızalı ürün takibini, stok yönetimini ve teknisyen işlemlerini kolaylaştırmayı amaçlar. Proje, [örneğin DevExpress, Entity Framework, MSSQL gibi] teknolojilerle geliştirilmiştir.

## Özellikler
- **Müşteri Yönetimi**: Müşteri bilgilerinin eklenmesi, güncellenmesi ve silinmesi.
- **Ürün ve Arıza Takibi**: Arızalı ürünlerin kaydı, arıza durumu takibi ve onarım süreç yönetimi.
- **Stok Yönetimi**: Yedek parça ve malzeme stoklarının takibi.
- **Teknisyen Yönetimi**: Teknisyen atama ve görev yönlendirme işlemleri.
- **Raporlama**: Servis işlemleri ve stok durumu için rapor oluşturma.

## Kullanılan Teknolojiler
- **C#**: Ana programlama dili
- **.NET Framework / .NET Core**: Uygulama çerçevesi
- **MSSQL**: Veritabanı yönetimi
- **[Opsiyonel] DevExpress**: Kullanıcı arayüzü bileşenleri
- **[Opsiyonel] Entity Framework**: Veritabanı işlemleri için ORM
- **Git**: Versiyon kontrol sistemi

## Kurulum

### Gereksinimler
- .NET Framework 4.8 veya .NET Core 3.1+ (projeye göre uyarlayın)
- Microsoft SQL Server 2019+
- Visual Studio 2019 veya üstü
- [Opsiyonel] DevExpress bileşenleri (kullanıyorsanız, lisanslı sürüm gerekebilir)

### Adımlar
1. **Depoyu Klonlayın**:
   ```bash
   git clone https://github.com/kullanici_adiniz/teknik-servis-otomasyonu.git
   ```
2. **Veritabanını Kurun**:
   - `database.sql` dosyasını SQL Server Management Studio (SSMS) ile çalıştırarak veritabanını oluşturun.
   - Veritabanı bağlantı dizesini `appsettings.json` veya `web.config` dosyasında güncelleyin:
     ```json
     "ConnectionStrings": {
       "DefaultConnection": "Server=localhost;Database=TeknikServisDB;Trusted_Connection=True;"
     }
     ```
3. **Bağımlılıkları Yükleyin**:
   - Visual Studio'da çözümü açın (`TeknikServis.sln`).
   - NuGet paketlerini geri yükleyin:
     ```bash
     dotnet restore
     ```
   - [Eğer kullanıyorsanız] DevExpress bileşenlerini projeye ekleyin.
4. **Projeyi Derleyin ve Çalıştırın**:
   - Visual Studio'da `F5` tuşuna basarak veya `dotnet run` komutuyla projeyi başlatın.

## Kullanım
1. **Giriş**: Uygulamayı başlattığınızda, varsayılan yönetici hesabıyla giriş yapabilirsiniz:
   - Kullanıcı Adı: `admin`
   - Şifre: `admin123`
2. **Müşteri Ekleme**: "Müşteri Yönetimi" sekmesinden yeni müşteri kaydı oluşturun.
3. **Arıza Kaydı**: "Arıza Takibi" sekmesinden yeni bir arıza bildirimi ekleyin ve teknisyen atayın.
4. **Raporlama**: "Raporlar" sekmesinden servis ve stok raporlarını görüntüleyin veya dışa aktarın.

## Proje Yapısı
```
├── TeknikServis.sln               # Çözüm dosyası
├── TeknikServis.Core/             # İş mantığı ve modeller
├── TeknikServis.Data/             # Veritabanı işlemleri (Entity Framework)
├── TeknikServis.UI/               # Kullanıcı arayüzü (WinForms/WPF/ASP.NET)
├── database.sql                   # Veritabanı şema dosyası
└── README.md                      # Proje dökümantasyonu
```

## Katkı Sağlama
1. Depoyu forklayın.
2. Yeni bir özellik dalı oluşturun: `git checkout -b ozellik/yeni-ozellik`.
3. Değişikliklerinizi yapın ve commit edin: `git commit -m "Yeni özellik eklendi"`.
4. Değişikliklerinizi push edin: `git push origin ozellik/yeni-ozellik`.
5. Bir Pull Request (PR) oluşturun.

## Lisans
Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

## İletişim
Sorularınız veya önerileriniz için enes.krkya1453@gmail.com adresine ulaşabilir veya GitHub Issues üzerinden bir sorun bildirebilirsiniz.
