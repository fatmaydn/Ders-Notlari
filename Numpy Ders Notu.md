# NumPy Ders Notu

### NumPy Nedir?
NumPy, Python'da bilimsel hesaplamalarda sıklıkla kullanılan temel bir pakettir. Çok boyutlu bir dizi nesnesi, çeşitli türetilmiş nesneler ve dizilerdeki hızlı işlemler için matematiksel, mantıksal, şekil işleme, sıralama, seçme girdi/çıktı içeren bir dizi yordam sunan bir Python kitaplıdır. Temel doğrusal cebir, temel istatistik işlemler, rassal simülasyon ve çok daha fazlası NumPy paketi ile kolayca gerçekleştirilebilmektedir.

### NumPy Listeleri vs Python Listeleri
* Python listeleri dinamik olarak büyüyebilen bir yapıya sahipken, NumPy listeleri sabit bir yapıya sahiptir. Bir NumPy listesine bir eleman eklediğinizde (boyutunu değiştirdiğinizde) ilk liste tamamen silinir ve yeni eklenen elemanlar ile liste yeniden oluşturulur. Bu sayede bilgisayar hafızasında daha az yer kaplar ve daha hızlı çalışır.

* NumPy listelerinde çok sayıda veri üzerinde gelişmiş matematiksel işlemler ve diğer işlemler kolaylıkla yapılabilir. Bazı işlemleri NumPy paketi kullanmadan yapmak oldukça zordur.

* NumPy listelerinde Python listelerinden farklı olarak her bir elemanın aynı türde olması ve sayısal veri olması gerekmektedir.

### NumPy Dizi Oluşturma
NumPy dizileri ile tek boyutlı (vektör), iki boyutlu (matris) ve daha çok boyutlu diziler oluşturulabilir ve bu diziler üzerinde aşağıdaki tabloda verilerin işlemler gerçekleştirilebilir.

|                                                      NumPy Metotları                                                      | Açıklaması                                                                                                                                    | Örnek Kullanımı                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------:|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| np.**array()**                                                                                                            | Listeyi NumPy dizisine dönüştürür.                                                                                                            | `d = np.array([1, 3, 5, 7])`                                                                      |
| np.**arange(**n**)**                                                                                                      | 0 - **n** _(n dahil değil)_ arası sayılardan<br>oluşan bir dizi oluşturur.                                                                    | `d = np.arange(5)`<br>`print (d)  #[0 1 2 3 4]`                                                   |
| np.**arange(**4, 20, 2**)**                                                                                               | Belirtilen aralıkta (4-20) artım miktarı (2 şer)<br>kadar **artan** sayılardan oluşan bir dizi oluşturur.                                     | `d = np.arange(4, 20, 2)`<br>`print (d)`<br>`# [4 6 8 10 12 14 16 18]`                            |
| np.**linspace(**0, 5, n**)**                                                                                              | Belirtilen aralıkta (0-5) **n** adet **eşit aralıklı<br>kesirli** sayılardan oluşan bir dizi oluşturur.                                       | `d = np.linspace(0, 5, 3)`<br>`print (d) #[0.0 2.5 5.0]`                                          |
| np.**logspace(**0, 2, n**)**                                                                                              | Belirtilen aralıkta (0-2) 10'un üssü şeklinde **n**<br>adet logaritmik sayılardan oluşan bir dizi oluşturur.                                  | `d = np.logspace(0, 2, 3)`<br>`print (d) #[1. 10. 100.]`                                          |
| np.**zeros((n, m)**, dtype=int**)**                                                                                       | İstenilen boyutta (_n satır, m sütunlu_) ve tipte<br>**sıfırlardan** (0) bir dizi/matris oluşturur.<br><br>dtype kullanımı zorunlu değildir.  | `d = np.zeros((2,3))`<br>`print (d)`<br>`# [[0. 0. 0.]`<br>    `[0. 0. 0.]]`                      |
| np.**ones((n, m)**, dtype=int**)**                                                                                        | İstenilen boyutta (_n satır, m sütunlu_) ve tipte <br>**birlerden** (1) bir dizi/matris oluşturur.<br><br>dtype kullanımı zorunlu değildir.   | `d = np.ones((2,3),dtype=int)`<br>`print (d)`<br>`# [[1 1 1]`<br>    `[1 1 1]]`                   |
| np.**full(**(n, m), a**)**                                                                                                | İstenilen boyutta (_n satır, m sütünlu_) tekrar eden<br>sayılardan **(s)** bir dizi/matris oluşturur.                                         | `d = np.full((2,3),6)`<br>`print (d)`<br>` # [[6 6 6]`<br>     `[6 6 6]]`                         |
| np.**repeat(**a, n**)**                                                                                                   | Tekrar eden sayılardan **(a)**, **n** elemanlı dizi<br>oluşturur.                                                                             | `d = np.repeat(3,4)`<br>`print (d)  #[3 3 3 3]`                                                   |
| np.**eye(**n, dtype=int)                                                                                                  | N elemanlı **birim matris** oluşturur.<br><br>dtype kullanımı zorunlu değildir.                                                               | `d = np.eye(3, dtype=int)`<br>`print(d)`<br>`# [[1 0 0]`<br>    ` [0 1 0]`<br>    ` [0 0 1]]`     |
| np.**trace**(d)                                                                                                           | Bir matrisin izini (köşegelnlerinin toplamını verir.)                                                                                         | `print(np.trace(d))  #3`                                                                          |
| np.**random.rand(n)**                                                                                                     | 0-1 arasında **n** adet rastgele (kesirli) sayılardan<br><br>oluşan bir dizi oluşturur.                                                       | `d = np.random.rand(5)`<br>`print(d)`<br>` # [0.45 0.76 0.61 0.33 0.67]`                          |
| np.**random.random(**n, m**)**                                                                                            | 0-1 arasında**n** satır, **m** sütunlu rastgele<br><br>(kesirli)sayılardan oluşan bir dizi/matris oluşturur.                                  | `d = np.random.random((2,3))`<br>`print(d)`<br>` # [[0.54 0.65 0.56]`<br>     `[0.91 0.50 0.99]]` |
| np.**random.rand(**n,m**)**                                                                                               | **n** satır, **m** sütunlu rastgele (kesirli)<br><br>sayılardan oluşan bir dizi oluşturur.                                                    | `d = np.random.randn(2,2)`<br>`print(d)`<br>` # [[1.54 -0.54]`<br>     `[3.03 0.40]]`             |
| np.**random.randint(**1,9,n**)**<br>#tek boyutlu dizi <br>veya<br>np.**random.randint(**1,9,[n,m]**)**<br>#2 boyutlu dizi | Belirtilen aralıkta (1-9) rastgele tam sayılardan<br><br>oluşan **n** adet bir dizi veya **[n,m]** adet matris<br><br>oluşturur.              | `d = np.random.randint(1,9,[2,5])`<br>`print(d)`<br>` # [[5 2 7 8 6]`<br>     `[7 7 6 5 4]]`      |




## Örnek Uygulamalar

----
##### Örnek 1
0 - 24 arasındaki çift sayılardan oluşan bir dizi tanımlayıp, ekranda gösteriniz.

##### Cevap 1
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np
d = np.arange(0, 24, 2)
print(d)
>[0 2 4 6 8 10 12 14 16 18 20 22]
```

</p>
</details>

---
##### Örnek 2
A dizisinin elemanlarını, ters sırada B dizisine kopyalayıp, ekranda gösteriniz.

##### Cevap 2
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np
A = np.arange(6) #A dizisi (0-5)
print(A)
> [0 1 2 3 4 5]
B = A[::-1] #B dizisi A dizisinin tersi
print(B)
>[5 4 3 2 1 0]
```
</p>
</details>

---
##### Örnek 3
Bir 4X4 birim matrisi oluşturup ekranda gösteriniz ve bu matrisin izini hesaplayınız.

##### Cevap 3
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np
d = np.eye(4, dtype=int)
print(d)
>[[1 0 0 0]
  [0 1 0 0]
  [0 0 1 0]
  [0 0 0 1]]
print("Matrisin izi:", np.trace(d))
> Matrisin izi: 4  
```
</p>
</details>

---

### NumPy Dizilerinde Kullanabileceğiniz İşlem Metotları
Diziler ile ilgili farklı işlemler gerçekleştirmek için yararlı olabilecek bazı metotlar aşağıdaki tabloda verişmiştir. Aşağıda belirtilen metotlar dışında python içinde varsayılan olarak kullanılan matematiksel fonksiyonlar da NumPy dizileri ile kullanılabilir.

NumPy dizi elemanlarına, liste elemanlarında olduğu gibi indir numaraları ile erişilebilir. NumPy dizilerinin boyutu eksen (axis)'ler ve rank(derece/yükseklik)'ler ile ifade edilebilir. NumPy dizilerinde bu eksenler "axis" parametresi ile ifade edilir. 2 boyutlu (matris) bir dizide sütunlar "axis=0",satırlar ise(axis=1) ile 3 boyulu (3D) bir dizide ise yüksekli (derece) "axis=0", sütunlar "axis=1", satırlar ise "axis=2" ile ifade edilir.

Aşağıdaki metotlar ile bir NumPy dizisinin farklı eksenleri (satır, sütün, yükseklik) üzerinde işlemler gerçekleştirilebilir.

|                               NumPy Metotları                               | Açıklaması                                                                                              | Örnek Kullanımı                                                                                                                                                                                                                                  |
|:---------------------------------------------------------------------------:|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d.**reshape(**n, m**)**<br><br><br>veya<br><br><br>a.**resize(**(n, m)**)** | Tek boyutlu **d** dizisini n satır, m sütunlu matrise<br>dönüştürür. Yani diziyi yeniden boyutlandırır. | `d = np.arange(6)`<br>`print(d)`<br>`# [0 1 2 3 4 5]`<br>`A = d.reshape(2,3)`<br>`print(A)`<br>`# [[0 1 2]`<br>    `[3 4 5 ]]`                                                                                                                   |
| A.**ravel()** veya<br><br>A.**flat**                                        | A matrisini tek boyutlu bir diziye dönüştürür.                                                          | `d = A.ravel()`<br>`print (d)  `<br>`#[0 1 2 3 4 5]`                                                                                                                                                                                             |
| A.**T**<br><br>veya<br><br>A.**transpose()**                                | A matrisinin transpose'sini alır. Yani satır ve <br>sütunların yerlerini değiştirir.                    | `c = A.T`<br>`print (c)`<br>`# [[0 3]`<br>`   [1 4]`<br>`   [2 5]]`                                                                                                                                                                              |
| d.**mean()**                                                                | Dizinin elemanlarının ortalamasını verir.                                                               | `d = np.array([1, 2, 3, 4])`<br>`ort = d.mean()`<br>`print (ort) #2,5`                                                                                                                                                                           |
| d.**sum()**                                                                 | Dizinin tüm elemanlarının toplamını verir.                                                              | toplam = d.sum()<br><br>`print(toplam) #10`                                                                                                                                                                                                      |
| d.**prod()**                                                                | Dizinin tüm elemanlarının çarpımını verir.                                                              | `carpim = d.prod()`<br>`print(carpim) #24`                                                                                                                                                                                                       |
| d.**cumsum(**axis=1**)**                                                    | Verilen eksendeki elemanlar (axis=1 için satırlar)<br>üzerinde birikimli toplama işlemi gerçekleştirir. | `d = np.array([[1, 2, 3],[4, 5, 6]])`<br>`print(d)`<br>`# [[1 2 3]`<br>`    [4 5 6]`<br>`t1 = d.cumsum(axis=1)`<br>`print(t1)`<br><br>`# [[1 3 6]`<br>    `[4 9 15]]`<br>`t2 = d.cumsum(axis=0)`<br>`print(t2)`<br>`# [[1 2 3]`<br>`   [5 7 9]]` |
| d.**cumprod(**axis=1**)**                                                   | Verilen eksendeki elemanlar üzerinde birikimli çarpma<br>işlemi gerçekleştir.                           | `c = d.cumprod(axis=1)`<br>`print (c)`<br>` # [[1 2 6]`<br>     `[4 20 120]]`                                                                                                                                                                    |
| d.**max(**axis=1**)**                                                       | Verilen eksendeki en büyük elemanı verir.                                                               | `max = d.max(axis=1)`<br>`print(max)  #[3 6]`<br># d matrisinin her bir satırındaki<br>en büyük değeri verir.                                                                                                                                    |
| d.**min(**axis=1**)**                                                       | Verilen eksendeki en küçük elemanı verir.                                                               | `min = d.min(axis=1)`<br>`print(min)`<br>`# [1 4]`                                                                                                                                                                                               |
| d.**argmax(**axis=1**)**                                                    | Verilen eksendeki en büyük değerdeki elemanın<br>indisini verir.                                        | `d.argmax(axis=1) #[2 2]`                                                                                                                                                                                                                        |
| d.**argmin(**axis=1**)**                                                    | Verilen eksendeki en küçük değerdeki elemanın<br>indisini verir.                                        | `d.argmin(axis=1)  #[0 0]`                                                                                                                                                                                                                       |
| np.**matmul**(a, b)                                                         | İki diziyi veya matrisi (a,b) çarpar.                                                                   | `a = np.array([3,5,9],[4,6,1],[1,8,2])`<br>`b = np.array([1,0,3],[4,5,7],[2,3,6])`<br>`c = np.matmul(a,b)`<br>`print(T)`<br>`# [[41 52 98]`<br>`   [30 33 60]`<br>`   [37 46 71]]`                                                               |
| np.**add**(a,b)                                                             | İki diziyi veya matrisi (a,b) toplar.                                                                   | `T = np.add(a,b)`<br>`print(T)`<br>`# [[4 5 12]`<br>`    [8 11 8]`<br>`    [3 11 8]]`                                                                                                                                                            |
| B = np.**copy(**A**)**                                                      | A dizinin tüm elemanlarını B dizisine kopyalar.                                                         | `d = np.array([1,2,3,4])`<br>`b = np.copy(d)`<br>`print(b)   #[1 2 3 4]`                                                                                                                                                                         |
| np.**unique(**d**)**                                                        | Bir dizideki tekil değerleri verir.                                                                     | `d = np.array([1,2,3,4,3,1,2])`<br>`print(np.unique(d))`<br>`# [1 2 3 4]`                                                                                                                                                                        |
| np.**where(koşul)**                                                         | Bir dizi üzerinde koşula bağlı işlem gerçekleştirir.                                                    | `d = np.arange(10)`<br>`print(np.where(d>5))`<br>`#[6 7 8 9]`                                                                                                                                                                                    |
| np.**intersect1d(**a,b**)**                                                 | İki veya daha fazla dizideki ortak elemanları verir.                                                    | `a = np.array([3,4,5,6,2])`<br>`b = np.array([3,4,0,6,7])`<br>`c = np.intersect1d(a,b)`<br>`print(c) # [3 4 6]`                                                                                                                                  |
| np.**setdiff1d(**a,b**)**                                                   | Birinci dizede olup, ikinci dizide olmayan elemanları<br>verir.                                         | `d = np.setdiff1d(a,b)`<br>`print(d) # [2 5]`                                                                                                                                                                                                    |
| d.**ptp()**                                                                 | Verilen eksendeki en büyük ve en küçük değer arasındaki<br>farkı verir.                                 | `d = np.array([3,4,1,6])`<br>`print(d.ptp())  # 5`                                                                                                                                                                                               |
| np.**sort(**d**)**                                                          | Verilen eksendeki elemanları sıralar                                                                    | `d = np.array([3,2,1],[0,5,4])`<br>`dSort = np.sort(d,Axis=None)`<br>`print(dSort)`<br>`#[0 1 2 3 4 5]`                                                                                                                                          |
| np.**searchsorted(**d, aranan**)**                                          | Sıralı bir dizide aranan elemanın indis numarasını <br>verir.                                           | `d = np.searchsorted([2,4,6],4)`<br>`print(d) #1`                                                                                                                                                                                             |

## Örnek Uygulamalar

----
##### Örnek 1
Üç boyutlu bir dizi tanımlayıp, bu diziyi sırası ile iki ve tek boyutlu diziye dönüştüren programı yazınız.

##### Cevap 1
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np
#Üç boyutlu dizi
c3 = np.array([[[0,1,2],[3,4,5],[6,7,8]],
[[9,10,11],[12,13,14],[15,16,17]],
[[18,19,20][21,22,23],[24,25,26]]])

print("c3:", c3.shape)
print(c3)

# Matrise dönüştürme
c2 = c3.reshape(3,9)

print("c2:", c2.shape)
print(c2)

# Diziye dönüştürme
c1 = c2.ravel()

print("c1:", c1.shape)
print(c1)

```
**Not:** 3 boyutlu dizi tanımlamasında; üç "[[[...]]]" köşeli parantez, 2 boyutlu dizide iki "[[..]]" köşeli parantez, tek boyutlu dizide bir "[.]" köşeli parantez kullanılır.

</p>
</details>

---

##### Örnek 2
**"d=[1,2,3,4,5,6,7,8,9,10,11,12]"** şeklindeki bir diziyi **3*4** lük bir matrise dönüştüren programı yazınız.

##### Cevap 2
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np

d = np.arange(1,13)

A = d.reshape(3,4)
print(A)
```
</p>
</details>

---

##### Örnek 3
İki matrisin toplam ve çarpım sonucunu ekranda gösteren programı yazınız.

##### Cevap 3
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np

a = np.array([[3,5,9],[4,6,1],[1,8,2]])
b = np.array([[1,0,3],[4,5,7],[2,3,6]])
cC = np.matmul(a,b) # Matrisin Çarpımı
cT = np.add(a,b)

print("a*b =\n", cC)
print("a+b =\n", cT)
````
</p>
</details>

---

##### Örnek 4
Bir matrisin satırları ile sütunlarını yer değiştiren programı NumPy kullanarak ve kullanmayarak yazınız.

##### Cevap 4
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np

A = [[0,1,2,3],[4,5,6,7],[8,9,0,22]]
# A nin transpozesi NumPy kullanmadan
B = []
for i in range(4):
  B.append([row[i] for row in A])
print("A'nın Transpozesi:\n", B)
# A nin transpozesi NumPy kullanarak
d = np.array(A)
B = d.T
print("A'nın Transpozesi:\n", B)
````
</p>
</details>

---

##### Örnek 5
0-100 arası rasgele tam sayılardan oluşan 24 elemanlı bir dizideki çift sayıları "0" karakteri ile yer değiştiren "tek" isimli bir dizi oluşturup, elemanlarını ekrana yazdırınız.

##### Cevap 5
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np

d = np.random.randint(0,100,24)
print(d)

tek = np.where(d % 2 !=0, d, 0)
print(tek)
````
</p>
</details>

---

##### Örnek 6
Bir matrisin elemanlarını **küçükten büyüğe doğru alt alta** ekrana yazdıran programı yazınız.

##### Cevap 5
<details><summary>Cevap</summary>
<p>

```Python
import numpy as np

a = np.array([[3,5,9],[4,6,1],[7,8,2]])
aS = np.sort(a,axis=None)
for i in aS.flat:
  print(i)
````
</p>
</details>

### Kaynak
[NumPy Dökümantasyon](https://numpy.org/doc/1.20/numpy-user.pdf)
