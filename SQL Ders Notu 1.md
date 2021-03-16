# MySQL Giriş Ders Notu

### SQL Nedir?

SQL (Structered Query Language) Veritabanı işlemleri için kullanılan bir alt dil olarak bilinmektedir. Verilerin belirli kriterlere göre sunulması işlemine sorgu denir. Sorgu işlemi ise SQL ile yapılabilmektedir. SQL Veritabanı sistemi bir programlama dili olarak bilinse de, aslında bir veritabanı yönetim sistemidir. Bilgisayarda dağınık olarak yer alan verilerin düzenlenerek depolanması için SQL veritabanı sistemi geliştirilmiştir.

### SQL Veritabanı Kullanımının Avantajları

- SQL Veritabanı bilgileri rahatlıkla kategorize edebilmektedir. Kategorik olarak depolanan bilgiler sayesinde dağınıklık ortadan kalkar. Ayrıca bir veriye ulaşmak çok daha kolay ve hızlı olacağından dolayı zamandan tasarruf sağlar.

- SQL sistemi sayesinde tekrar eden verilerden kurtulunmuş olacaktır.

- Bilgisayar hafızasında dağınık halde bulunan bilgilerin klasöre dönüştürülebilmesine yardımcı olur. Bu sayede boş yer işgalinin önüne geçilmiş olur.

- Bütün veritabanı işlemlerinde SQL sistemine ihtiyaç duyulmaktadır. SQL veritabanının temel amacı, hem verilerin hem de veri kümelerinin modellenmesini sağlamaktır.

### SQL Veritabanı Kullanılarak Yapılabilecek İşlemler

- Yeni veriler çekmek

- Var olan verileri kaydetmek

- Verilerin tamamını güncellemek

- Verilerin sorgulanmasını ve aramasını yapmak

- Silinen verilerin kayıtlarını yeniden oluşturulmasını sağlamak

- Güvenlik ayarları yapmak

- Yeni tablolar oluşturmak

### SQL ile Sorgulama Yapan Yazılımlar

- Oracle SQL: Veritabanı yazılım sistemleri arasında en güçlü olan yazılımdır. Bütün büyük firmalar ve uygulamalarda kullanılabilmektedir.

- Microsoft SQL Server (MSSQL): Sunucu tabanlıdır ve Microsoft tarafından geliştirilmiştir. SQL sistemi kullanarak işlemler yapılmaktadır.

- MySQL: Hem ücretsiz hem de açık kaynaklı olan bir SQL sistemidir. Bu sistemin geliştiricisi Oracle'dır.

- Access: Bu sistem de Microsoft tarafından geliştirilmiştir. Diğer sistemlere göre daha küçük olan uygulamalar için geliştirilmiştir.


## MySQL Kurulumu

Öncelikle [burada belirtilen linkten](https://dev.MySQL.com/downloads/windows/installer/8.0.html) MySQL indirme sayfasına gidiniz. Burada karşınıza iki tane versiyon çıkacaktır. Bir tanesi düşük boyutlu bir tanesi ise yüksek boyutlu olandır. Burada yüksek boyutlu olan dosyanın yanındaki download butonundan dosyayı indiriyorsunuz.

![Image 1](https://i.imgur.com/jw92hvu.png "Yüksek Boyutlu Dosya")

Belirtilen yerden dosyayı indirmeniz uzun sürebilir ancak kurulum aşaması çok daha kısa sürecektir. Dosyayı bilgisayarınıza indirikten sonra açtığınızda karşınıza aşağıdaki gibi bir ekranın çıkması gerekmektedır.

![Image 2](https://i.imgur.com/MnlGyI7.png "Ana Kurulum Ekranı")

Burada "FULL" yazan versiyonu seçmeniz gerekmektedir. FULL versiyonunu seçtikten sonra "NEXT" ile devam edebilirsiniz.

![Image 3](https://i.imgur.com/EM1NjA2.png "Gerekli Programların Kontrolü")

Burada ekran karşınıza çıktığında "NEXT" ile devam edebilirsiniz. Bilgisiyarınıza Visual Studio yüklü ise bu ekran karşınıza çıkmayacaktır.

![Image 4](https://i.imgur.com/UivalTv.png "VS Hatası")

Next'e tıkladıktan sonra karşınıza bu şekilde bir hata çıkacaktır burada "YES" ifadesine tıklayarak devam ediniz.

![Image 4](https://i.imgur.com/pdDkHJq.png "Execute Ekranı")

Yes ifadesine tıkladıktan sonra karşınıza bu ekranın çıkması gerekmektedir. Bu ekranda "EXECUTE" butonuna tıklayarak yükleme işlemini başlatabilirsiniz.

![Image 4](https://i.imgur.com/XubZnqr.png "Complete")

Bütün yüklemeler tamamlandıktan sonra "NEXT" butonuna tıklayarak işleme devam edebilirsiniz. Daha sonra karşınıza aşağıdaki bir ekran çıkacaktır. Burada da "NEXT" ifadesine tıklayarak işleme devam edebilirsiniz.

![Image 4](https://i.imgur.com/KOmeDst.png "Configure")

Next ile bir sonraki ekrana geçtikten sonra karşınıza aşağıdaki gibi bir ekran çıkacaktır. Burada hiçbir ayarı değiştirmeden "NEXT" ile bir sonraki adıma geçiyoruz.

![Image 4](https://i.imgur.com/J9wZ613.png "Networking")

Bir sonraki adımda da herhangi bir değişiklik yapmadan "NEXT" ile bir sonraki adıma devam ediyoruz.

![Image 4](https://i.imgur.com/0xSGL85.png "Password")

Bu adımda MySQL SERVER için bir adet ROOT parolası belirlemeniz gerekmektedir. MySQL Root Password alanına istediğiniz bir şifreyi giriyorsunuz. Daha sonrasında Repeat Password kısmına da MySQL Root Password kısmına girmiş olduğunuz şifreyi tekrardan giriyorsunuz. Eğer iki şifre birbiri ile aynı ise aşağıdaki "NEXT" butonu aktif olacaktır ve bu butona tıklayarak bir sonraki adıma geçebilirsiniz.

![Image 4](https://i.imgur.com/1LAkZsK.png "Server Name")

Bu adımda da herhengi bir değişiklik yapmadan "NEXT" butonuna tıklayarak işleme devam ediyoruz.

![Image 4](https://i.imgur.com/TNSXnHQ.png "Apply Configure")

Karşımıza çıkan bu adımda "EXECUTE" butonuna tıklayarak belirtmiş olduğumuz ayarların SERVER'a yüklenmesini sağlıyoruz.

![Image 4](https://i.imgur.com/ZALfFuI.png "Apply Configure")

Server ayarlarının kurulumu tamamlanmış oldu şimdi "FINISH" butonuna tıklayarak bir sonraki adıma geçebilirsiniz.

![Image 4](https://i.imgur.com/oXbXWro.png "Product Configure")

Karşımıza çıkan bu ekranda da "NEXT" tuşuna basarak bir sonraki adıma ilerleyebilirsiniz.

![Image 4](https://i.imgur.com/uAMgnpu.png "Router Configure")

Router ayarlarının kurulumu tamamlanmış oldu şimdi "FINISH" butonuna tıklayarak bir sonraki adıma geçebilirsiniz.

![Image 4](https://i.imgur.com/48AFQcn.png "Product Configure")

Karşımıza çıkan bu ekranda da "NEXT" tuşuna basarak bir sonraki adıma ilerleyebilirsiniz.

![Image 4](https://i.imgur.com/45zzIqc.png "Server Check")

Bu adımda daha önceden belirlemiş olduğumuz ROOT şifresini girerek "CHECK" butonuna tıklıyoruz. Girdiğiniz bilgilerin doğru olması durumunda "NEXT" butonu aktif olacaktır. "NEXT" tuşuna tıklayarak bir sonraki adıma geçebilirsiniz.

![Image 4](https://i.imgur.com/jqmdD7R.png "Product Configure")

Karşımıza çıkan bu adımda "EXECUTE" butonuna tıklayarak belirtmiş olduğumuz ayarların SERVER'a yüklenmesini sağlıyoruz.

![Image 4](https://i.imgur.com/yearDIm.png "Product Configure")

Ürün ayarlarının kurulumu tamamlanmış oldu şimdi "FINISH" butonuna tıklayarak bir sonraki adıma geçebilirsiniz.

![Image 4](https://i.imgur.com/LcV6T0N.png "FINISH")

Karşımıza çıkan ekranda "NEXT" butonuna tıklayarak tüm adımları bitirebilirsiniz.

![Image 4](https://i.imgur.com/xhbOVGk.png "FINISH")

Karşımıza çıkan ekranda "FINISH" butonuna tıklayarak kurulumu bitirebilirsiniz. MySQL ve diğer kullanacağımız araçları başarı ile bilgisayarınıza yüklemiş oldunuz.

## Syntax Kullanımı

SQL dilinde kodları büyük küçük harf duyarsız şekilde yazabilirsiniz ancak bu genellikle tercih edilmeyen bir şeydir. Genel olarak SQL dilinde KOMUTLAR BÜYÜK HARFLER, tablo ve sütunlar küçük harfler ile kodlanırlar daha rahat anlaşılabilmesi için.

```SQL
Select * From Ogrenciler; # Tercih edilmeyen kullanım
SeLEcT * fROm oGreCilER; # Tercih edilmeyen kullanım

SELECT * FROM ogrenciler # Tercih edilen kullanım
"String değerler tek tırnak veya çift tırnak ile gösterilmelidir"
```
Herkesin kullanmış olduğu yazım kurallarını kullanırsanız hem daha rahat hem de başkaları tarafından daha kolay okunabilir bir kod yazmış olursunuz.

## Database Kodları

#### Database Oluşturma
```SQL
CREATE DATABASE test;
```
Bu kod sayesinde SQL Server'a test adlı bir database oluşturmuş oluyoruz. *__CREATE__* komutunu kullandıktan sonra database oluşturulmuş oluyor. *__CREATE__* komutu sistemi otomatik olarak refreshlemediği için **"SCHEMAS"** alanında oluşturmuş olduğunuz database gözükmeyecektir. **"SCHEMAS"** alanındaki **refresh** tuşuna basmanız gerekmektedir. Eğer Serverda ismi olan bir database oluşturmaya çalışırsanız aşağıdaki gibi bir hata alırsınız bundan dolayı böyle bir hata alıyorsanız mutlaka **"SCHEMAS"** kısmını kontrol ediniz.

![Image 4](https://i.imgur.com/ayFXz2R.png "Error Code: 1007")

#### Database Silme
```SQL
DROP DATABASE test;
```
Bu kod sayesinde SQL Server'da test adlı bir database'i silmiş oluyoruz. **DROP DATABASE** komutu database'i komple silmektedir buna içindeki **tablo ve verilerde dahildir**. Bundan dolayı normal şartlarda asla kullanılmaması gereken bir komuttur. Eğer Serverda ismi olmayan bir database'i silmeye çalışırsanız aşağıdaki gibi bir hata alırsınız bundan dolayı böyle bir hata alıyorsanız mutlaka **"SCHEMAS"** kısmını kontrol ediniz.

![Image 4](https://i.imgur.com/eYVtTF4.png "Error Code: 1008")

#### Database'i Aktif Hale Getirmek
```SQL
USE test;
```
Bu kod sayesinde belirttiğimiz database aktif hale gelir. Aktif hale gelmiş bir database **SCHEMAS** alanında kalın bir hale gelir. Bu sayede database'in içinde bulunan tablo ve verilere ulaşabiliriz.

![Image 4](https://i.imgur.com/CDYqw8Z.png "Error Code: 1008")

#### Tablo Oluşturmak
```SQL
CREATE TABLE test(
  test_sutun INT
);
```
Tablo oluşturmak database oluşturmanın birbirine benzer bir yapıdadır. Ancak tabloları oluştururken tablolarda bulunacak sütünları ve sütünların özelliklerini de belirtmek gerekmektedir.

#### Var Olan Bir Tabloyu Güncellemek
```SQL
ALTER TABLE test ADD yeni_sutun VARCHAR(255);
```
**ALTER TABLE** komutu ile var olan bir tabloyu güncelleyebilirsiniz. Tabloya yeni bir sütun ekleyebilir veya tablodan bir sütun çıkartabilirsiniz.

#### Tablo Silme
```SQL
DROP TABLE test;
```
Bu kod sayesinde database de bulunan test adlı bir tabloyu silmiş oluyoruz. **DROP TABLE** komutu tabloyu komple silmektedir buna içindeki **veriler de dahildir**. Bundan dolayı normal şartlarda asla kullanılmaması gereken bir komuttur.


# Öğrenci Sistemi
```SQL
CREATE DATABASE ogrenci_sistemi;

USE ogrenci_sistemi;

CREATE TABLE ogrenci_bilgileri(
  id INT NOT NULL AUTO_INCREMENT,
  ogrenci_adi VARCHAR(255) NOT NULL,
  ogrenci_numarasi INT NOT NULL,
  kayit_tarihi DATETIME,
  PRIMARY KEY (id)
);
```
Bu kod sayesinde **ogrenci_bilgileri** adlı bir tablo oluşturduk ve bu tablonun içinde **id** sütunu bulunmakta integer yapıda boş bir değer olamayan ve her yeni kayıtta otomatik olarak artan bir yapısı bulunmaktadır. Yeni bir öğrenci tanımladığınızda sistem id yi otomatik olarak verir siz bir değer girmezsiniz. **Ogrenci_adi** adlı bir sütun bulunmakta ve bu karakter yapısında bir sütün ve maksimum 255 karakter girilebilmektedir ve yine bu sütun da boş bırakılamaz. **Ogrenci_numarasi** adlı bir sütun bulunmakta ve buraya öğrencinin numarasının girilmesi gerekmektedir ve boş bırakılamaz. **Kayit_tarihi** adlı bir sütun bulunmakta ve ogrencinin kayıt yaptırdığı tarih girilebilir ancak istenirse boş da bırakılabilir. **PRIMARY KEY** bir tablodaki benzersiz alanı göstermektedir. Hiçbir kayıtta aynı olamayacak alanlardır. Bir kaydın eşleniksiz karşılığıdır.

```SQL
CREATE TABLE dersler(
  id INT NOT NULL AUTO_INCREMENT,
  ders_adi VARCHAR(255) NOT NULL,
  ders_donemi VARCHAR(25) NOT NULL,
  ders_gunu VARCHAR(10),
  PRIMARY KEY (id)
);

CREATE TABLE kayitlar(
  id INT NOT NULL AUTO_INCREMENT,
  ogrenci_id INT NOT NULL,
  ders_id id NOT NULL,
  vize INT,
  final INT,
  genel INT,
  harf_notu VARCHAR(5),
  PRIMARY KEY (id),
  FOREIGN KEY (ogrenci_id) REFERENCES ogrenci_bilgileri(id),
  FOREIGN KEY (ders_id) REFERENCES dersler(id)
);
```
Burada **dersler** ve **kayitlar** adlı iki tablo oluşturduk. Her tabloya bir adet **PRIMARY KEY** belirledik. **FOREIGN KEY** eğer tablodaki alan aslında başka bir tablo ile ilişkili ise bu ilişkinin belirtilmesi için kullanılmaktadır. Örneğin **FOREIGN KEY (ogrenci_id) REFERENCES ogrenci_bilgileri(id)** kodu **kayitlar** tablosunda bulunan **ogrenci_id** sutunundaki değerlerinin **ogrenci_bilgileri** tablosunda bulunan **id** alanı ile ilişkili olduğunu belirtmek için kullanılmaktadır.  
