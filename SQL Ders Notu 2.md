# MySQL Giriş Ders Notu 2

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
