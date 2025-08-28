## TEMEL LİNUX KOMUTLARI

Linux Dosya Yapısı

```markdown
/               -> Kök dizini
├── bin/        -> Temel kullanıcı komutları (ls, cp, mv, cat, …)
├── boot/       -> Çekirdek ve önyükleme dosyaları (kernel, grub)
├── dev/        -> Donanım aygıt dosyaları (/dev/sda, /dev/null)
├── etc/        -> Sistem yapılandırma dosyaları/konfigürasyon (/etc/passwd, /etc/hosts)
├── home/       -> Kullanıcıların ev dizinleri (/home/ali, /home/bugra)
├── lib/        -> Paylaşımlı kütüphaneler (.so dosyaları)
├── media/      -> Çıkarılabilir ortamlar (USB, CD, DVD)
├── mnt/        -> Geçici bağlama noktaları (mount edilen dosya sistemleri)
├── opt/        -> Opsiyonel yazılımlar (3. parti paketler)
├── proc/       -> Çalışan süreçler ve sistem bilgileri (sanal dosya sistemi)
├── root/       -> Root kullanıcısının ev dizini
├── run/        -> Geçici çalışma zamanı dosyaları (PID dosyaları vs.)
├── sbin/       -> Sistem yönetim komutları (ifconfig, shutdown, …)
├── srv/        -> Sunucu servis verileri (örn: web, ftp)
├── sys/        -> Donanım ve çekirdek bilgileri
├── tmp/        -> Geçici dosyalar (yeniden başlatınca silinir)
├── usr/        -> Kullanıcıya ait uygulamalar ve kütüphaneler
│   ├── bin/    -> Kullanıcı uygulamaları (ls, grep, awk, …)
│   ├── sbin/   -> Yönetim uygulamaları
│   ├── lib/    -> Kütüphaneler
│   └── share/  -> Paylaşılan dosyalar (dökümantasyon, ikonlar)
└── var/        -> Değişken dosyalar (loglar, spool, cache)
    ├── log/    -> Sistem log dosyaları
    ├── mail/   -> E-posta verileri
    ├── spool/  -> Yazıcı ve e-posta kuyrukları
    └── tmp/    -> Geçici dosyalar

```


$ : Sizin sıradan (normal) kullanıcı olduğunuzu belirtir.

\# : Süper kullanıcı (root) olduğunuzu belirtir.

~ : Kullanıcının ev dizininde bulunduğunuzu belirtir

/ : Kök dizin (en üst seviye)

. : Bulunduğun mevcut dizin

.. : Bir üst dizin

\- : Bir önce bulunduğun dizin

~kullanici : Belirtilen kullanıcının home dizini (örn: ~root → /root)


### Linux Komut Yapısı

komut [seçenekler] [argümanlar]

Komut: Komutun kendisidir (işlev).

Seçenekler (Options): Komutun işlevini değiştirmeye yarar.  (-) işareti ile başlar.Uzun yazılış: Çift tire (--) tamamı yazarız.

* örnek

   -v  --verbose	İşlemin aşamalarını ayrıntılı 	gösterir.

Argümanlar (Arguments): Komutun üzerinde işlem yapacağı nesnedir. Örneğin dosya



---

# Linux Komutları ve Seçenekleri
## Seçenekler
- `-h`, `--help` → Komutun yardım ekranını gösterir  
- `-v`, `--version` → Komutun sürümünü gösterir  
- `-r` → Recursive (özyinelemeli işlem)  
- `-f` → Force (zorla çalıştırma)  
- `-i` → Interactive (işlemden önce sorar)  
- `-q` → Quiet (sessiz mod)  
- `-n` → Satır/limit belirtme (örn: `head -n 5`)  

# Linux Komutları

## 📂 ls (listeleme)

| Komut               | Açıklama                         |
|----------------------|----------------------------------|
| `ls`                | Bulunduğun dizindeki dosyaları listele |
| `ls -l`             | Ayrıntılı listeleme (izinler, boyut vb.) |
| `ls -a`             | Gizli dosyaları da göster        |
| `ls -la`             | Gizli dosyaları ayrıntılı listele        |
| `ls -lh`            | Boyutları okunabilir formatta    |
| `ls -laR `            | Boyutları okunabilir formatta    |
| `ls -l -a -R `         | Yukarıdakinden farkı yok
| `ls -R`             | Alt dizinleri de listele         |
| `ls -lt`             |  komutu dosyaları/dizinleri son değişiklik tarihine göre sıralar  |

---

## 📂 mkdir (Klasör oluşturma)

| Komut               | Açıklama                         |
|----------------------|----------------------------------|
| `mkdir -p ` | seçeneği ile kullanılarak tek bir seferde iç içe birden fazla dizin oluşturulabilir. |
| `mkdir --mode` |kullanıcının istediği erişim haklarına sahip dizinler yaratılabilir. |


## 📂 rmdir (Klasör silme)
rmdir komutu içi boş bir dizini silmek amacıyla kullanılır.

## rm (remove) Komutu
rm komutu dosya veya dizin silmek için kullanılır.

## mv (move) Komutu
Bir dosyanın/klasörün ismini değiştirmek ya da bir dosyayı/klasörü taşımak için mv komutu kullanılır. 

## 📄 cp (dosya kopyalama)

| Komut                   | Açıklama                        |
|--------------------------|---------------------------------|
| `cp dosya hedef/`       | Dosyayı hedefe kopyala          |
| `cp -r dizin hedef/`    | Dizini içindekilerle kopyala    |
| `cp -i dosya hedef/`    | Üzerine yazmadan önce sor       |
| `cp -f dosya hedef/`    | Zorla kopyala                   |
| `cp -v dosya hedef/`    | Kopyalanan dosyaları göster     |

---

## ✂️ rm (dosya/dizin silme)

| Komut                  | Açıklama                         |
|-------------------------|----------------------------------|
| `rm dosya.txt`          | Dosya sil                       |
| `rm -i dosya.txt`       | Silmeden önce sor                |
| `rm -f dosya.txt`       | Onay sormadan sil                |
| `rm -r dizin/`          | Dizini ve içindekileri sil       |
| `rm -rf dizin/`         | Onaysız, dizini komple sil       |




---

## 📑 cat / head / tail (dosya görüntüleme)

| Komut              | Açıklama                         |
|---------------------|----------------------------------|
| `cat dosya.txt`     | Dosyanın tamamını göster         |
| `cat -n  dosya.txt`     | Satırları numaralar.        |
| `cat > dosya.txt`     | dosya.txtnin içindeki metni sil yeni metni ekle     |
| `cat >> dosya.txt`     | dosya.txtnin içindeki metnin sonuna ekle   
| `head dosya.txt`    | İlk 10 satırı göster             |
| `head -n 5 dosya`   | İlk 5 satırı göster              |
| `tail dosya.txt`    | Son 10 satırı göster             |
| `tail -f dosya.txt`    | evamlı güncellenen log dosyalarını izlemek için kullanılır.   Ctrl+C ile sonlandırılır.         |

| `tac` | Dosya içeriğini ekrana tersten yazdırır.   |


---

## 🔍 grep (arama)

| Komut                         | Açıklama                            |
|-------------------------------|-------------------------------------|
| `grep kelime dosya.txt`       | Dosya içinde kelime ara             |
| `grep -i kelime dosya.txt`    | Büyük/küçük harf duyarsız arama     |
| `grep -r kelime /dizin/`      | Dizin içinde özyinelemeli arama     |
| `grep -n kelime dosya.txt`    | Satır numarasıyla göster            |

---
## echo(ekrana yazdırma) 
echo komutu Linux’ta ekrana çıktı vermek için kullanılır.
```bash
echo Merhaba Dünya
```
### Değişkenlerle Kullanım:
```bash
NAME="Bugra"
echo Merhaba $NAME
```
### Tık tırnak çift tırnak meselesi
Tek tırnak:

1. İçindeki her şeyi olduğu gibi yazar.

2. Değişkenler, $, \n, \t gibi özel karakterler çalışmaz.
```bash
NAME=Bugra
echo 'Merhaba $NAME'
```
Çıktı:

Merhaba $NAME

Çift Tırnak

1. İçindeki değişkenleri ve özel karakterleri işler.

2. Yani $ ile başlayan değişkenler yerine değerini koyar.
```bash
NAME=Bugra
echo "Merhaba $NAME"
```
Çıktı:

Merhaba Bugra


# Linux Kontrol Karakterleri

Linux ve Unix sistemlerinde terminal ve kabukta kullanılan bazı kontrol karakterleri şunlardır:

| Kontrol Karakter | Tuş Kombinasyonu | Açıklama |
|-----------------|-----------------|----------|
| `^C`            | Ctrl + C        | Çalışan işlemi durdurur 
| `^Z`            | Ctrl + Z        | Çalışan işlemi arka plana gönderir (suspend) |
| `^D`            | Ctrl + D      ▶️  | Girdi sonu (EOF), terminali kapatır veya girişi bitirir |
| `^S`            | Ctrl + S        | Terminali durdurur (flow control – durdurma) |
| `^Q`            | Ctrl + Q        | Terminali yeniden başlatır (flow control – devam) |
| `^U`            | Ctrl + U     ▶️   | Satırın başına kadar siler |
| `^K`            | Ctrl + K        | İmleçten satır sonuna kadar siler |
| `^W`            | Ctrl + W    ▶️    | Son kelimeyi siler |
| `^L`            | Ctrl + L    ▶️    | Terminal ekranını temizler (clear) |
| `^R`            | Ctrl + R        | Komut geçmişinde arama yapar |
| `^A`            | Ctrl + A     ▶️   | Satır başına gider |
| `^E`            | Ctrl + E      ▶️  | Satır sonuna gider |

> Not: `^` işareti, Ctrl tuşu ile birlikte basıldığını gösterir.

# Man Sayfasında Gezinme
* spacebar man sayfasının bir sonraki ekranını gösterir.

* return her basışta bir satır gösterir.

* b / PgUp bir ekran öncesine döner.

* f / PgDown bir ekran sonrasına gider.

* q man sayfasından çıkar.

*  /kelime yazılan kelimeyi bulunulan yerden itibaren ileriye doğru arar.

* /kelime yazılan kelimeyi bulunulan yerden itibaren ileriye doğru arar.

*  n aranan kelimenin bir sonraki geçtiği yeri gösterir.

* h tüm bu işlemler için yardım sunar.


# less Komutu
Dosya içeriğini sayfa sayfa veya satır satır gösterir.

Hareketler:

* spacebar		:	Bir sayfa ileri.

* enter	    		:	Bir satır ileri.

* b					:	Bir sayfa geri.

* q					:	Çık.

* /kelime		:	Belirtilen kelimeyi ara.

* n					:	Son aramayı yinele.

# Dosya Yolları

* Mutlak (Tam):	Kök klasöründen (/) başlayarak.

* Bağıl:				Bulunulan dizine göre. 

* .				:	İçinde bulunulan klasör.

* ..				:İçinde bulunulan klasörün bir üst klasörü.

* \-				:	Bir önceki klasör.

* ~				:	Mevcut kullanıcının ev klasörü.

* ~kullanıcı	:	Belirtilen kullanıcının ev klasörü.

* /   			:    Kök klasörü (dizini)









## Birkaç Örnek Komut

ls -la  ~/Desktop/kabuk masaüstündeki kabuk klasörünün içini detaylı listelerken gizli dosyalrıda göster.

ls -lt komutu dosyaları/dizinleri son değişiklik tarihine göre sıralar ve listeler.

~$ pwd normal kullanıcının home dizinin yolunu göster.

~# pwd root kullınıcısının ev dizinin göster.

cd /var/log  kök dizin → var dizini → log dizini.

cd ../.. komutu, bulunduğun dizinin bir üstünün bir üst dizinine geçer.

cd  ~ Direkt olarak kendi ev dizininize gidebilirsiniz.

cd   ~bugor bugor kullanıcısının kök dizini

cd   - En son bulunduğunuz dizine geri dön.

head -n 3 dosyaAdi  dosyanın ilk 3 satırını gösterir.

head -n -3 dosyaAdi son 3 satır hariç tümünü gösterir.


tail -n 3 dosyaAdi Dosyanın son 3 satırını gösterir.

tail -n +3 dosyaAdi Dosyanın 3. satırdan başlayarak sonuna kadar tümünü gösterir.

mv deneme.txt ~/Desktop deneme.txtyi desktop a taşı


---



# Erişim İzinleri


<img src="./assets/Erişimİzinleri.PNG" alt="alt yazı" width="500">

1️⃣ İzin Türleri

r (read) → okuma izni  /içeriğinin görüntülenmesine ve kopyalanmasına izin verilmesi

w (write) → yazma  /değiştirme izni  /içeriğinin değiştirilebilmesine ve silinebilmesine izin verilmesi

x (execute) → çalıştırma izni

2️⃣ Kullanıcı Grupları

Her dosya/klasör için izinler 3 farklı gruba tanımlanır:

Owner (kullanıcı / u) → dosyanın sahibi

Group (g) → dosyanın ait olduğu grup

Others (o) → diğer tüm kullanıcılar

Dosyaların ve dizinlerin erişim haklarını dosya ve dizin sahipleri ile sistemin root kullanıcısı değiştirebilir.

#### Örnek:

-rwxr-xr--

\- → dosya (d olsaydı klasör)

rwx → sahibi (user) okuma, yazma, çalıştırma yapabilir

r-x → gruptakiler okur ve çalıştırır ama yazamaz

r-- → diğer kullanıcılar sadece okuyabilir


Erişim hakkı değiştirme
```bash
chmod u+x dosya.sh   # Kullanıcıya çalıştırma izni ekler
chmod g-w dosya.txt  # Gruptan yazma iznini alır
chmod o=r dosya.txt  # Diğerleri sadece okuma yapabilir
```
Sayısal yöntem

r = 4	

w = 2	

x = 1
```bash

chmod 755 dosya.sh
```
7 = rwx (4+2+1) → kullanıcı

5 = r-x (4+1) → grup

5 = r-x (4+1) → diğerleri


Sahiplik Değiştirme
1️⃣ Kullanıcı değiştirme
```bash
chown ali dosya.txt
```
2️⃣ Kullanıcı + Grup değiştirme
```bash
chown ali:ogrenci dosya.txt
```
3️⃣ Sadece grup değiştirme
```bash
chown :ogrenci dosya.txt
```
4️⃣ Klasör ve içindekiler için (recursive)
```bash
chown -R ali:ogrenci /home/proje
```
📌 /home/proje klasörü ve içindeki tüm dosyaların sahibi ali:ogrenci yapılır.

4️⃣ Numara ile değiştirme 

chown  kullaniciNo:grupNo  dosyaAdi
```bash
chown  620:100 deneme.txt
```
# Wildcards
Komut satırında kullanılan ve Linux komutlarına argüman olarak verilebilecek özel semboller vardır.

Bu özellik, özellikle dosya arama, kopyalama, taşıma ve silme işlemlerinde çok faydalıdır.

#### \* → Sıfır veya daha fazla karakter
```bash
ls *.txt  # txt dosyalarını listele
```
a* yazımı, a karakteri ile başlayan bütün sözcükleri gösterir: a, araclar, a75 gibi...

*z yazımı ise z karakteri ile biten bütün sözcükleri ifade eder: z, az, a95z gibi...

re*m yazımı, re ile başlayıp m ile biten sözcükleri tanımlar: rem, resim, rengim, re57m gibi...
```bash

# İçinde "log" geçen tüm dosyalar
ls *log*
```
####  ? → Tek karakter/ boşluk ifadesi yok

```bash
ls ?.txt #Sadece tek karakterli dosya isimleri (a.txt, b.txt) eşleşir.
```
a? yazımı, a harfi ile başlayan 2 karakterli sözcükleri ifade eder. Burada (?) tek bir karakter yerine geçer: ab, a2, a+ gibi…

####  [] → köşeli parantez içerisindeki karakterlerden herhangi biri/boşluk ifadesi yok

```bash
ls file[1-3].txt #file1.txt, file2.txt, file3.txt ile eşleşir.
```

#### [! ] → Hariç tutma
```bash

ls file[!0-9].txt #İsmi file ile başlayıp son karakteri rakam olmayan dosyaları listeler.
```
#### { } → Küme parantezi ile seçenekler
```bash
ls {a,b,c}.txt #a.txt, b.txt, c.txt dosyalarıyla eşleşir.
```
```bash
ls [A-Z]* #Büyük harfle başlayan dizinler
```
```bash
ls D* # Bu komut "D" ile başlayan her şeyi listeler, ama dizinlerin içeriğini de gösterir:
```

Çıktısı

Documents:
file1.txt  file2.txt  subfolder/

Downloads:
movie.mp4  song.mp3  archive.zip

Desktop:
shortcut1  shortcut2  readme.txt

```bash
ls -d D* # Bu komut sadece dizin isimlerini listeler, içeriklerine girmez:
```
```bash
ls -d */  # Tüm dizinleri listele (içerik gösterme)
```


### NOT
Bunlar dosyaları listeler veya hiçbirini  bulunamazsa bir hata döndürür.
```bash
ls  *.txt  2>/dev/null
```

2>/dev/null: Komutun bu kısmı, stderr'i (hata mesajlarını) üzerine yazılan tüm verileri çöpe atan özel bir dosya olan /dev/null'a yönlendirir. Bu ise, ls'den gelen muhtemel hataları gizler.


###  expr (evaluate expressions) Komutu
Boşluklara dikkat edilerek
```bash
# Toplama
expr 5 + 3        # Çıktı: 8

# Çıkarma
expr 10 - 4       # Çıktı: 6

# Çarpma (dikkat: * escape edilmeli)
expr 6 \* 7       # Çıktı: 42

# Bölme (integer division)
expr 15 / 3       # Çıktı: 5
expr 17 / 3       # Çıktı: 5 (kalan atılır)

# Mod (kalan)
expr 17 % 3       # Çıktı: 2

# Karşılaştırma İşlemleri
expr 5 = 5

a=10
b=3
expr $a + $b

 
```
boşluksuz 
```bash

ddal@admin~ $ echo `expr   3   \*   4`
12
ddal@admin~ $ sayi=`expr   3   \*   5`
ddal@admin~ $ ((sayi++))
ddal@admin~ $ echo $sayi
16
```

expr için mantıksal VEYA | dir. Pipe karakteri ile karıştırılmasın diye \| şeklinde kullanılmalıdır.

expr için mantıksal VE & dir. Background process karakteri ile karıştırılmasın diye \& şeklinde kullanılmalıdır.

expr için küçüktür < dir. Yönlendirme karakteri ile karıştırılmasın diye \< şeklinde kullanılmalıdır.

expr için büyüktür > dir. Yönlendirme karakteri ile karıştırılmasın diye \> şeklinde kullanılmalıdır.


## String (Metin) İşlemleri
```bash
expr length "Bugra"
```
çıktı 
5
```bash
expr substr "BugraChat" 2 3
```
çıktı
ugr
```bash
expr index "Linux" n 
```
Çıktı: 
3 
(çünkü n 3. sırada)


##  Girdilerin ve Çıktıların Yönlendirilmesi
Standart girdi (stdin) → 0 ile temsil edilir (klavyeden gelen veri).

Standart çıktı (stdout) → 1 ile temsil edilir (ekrana yazılan normal çıktı).

Standart hata (stderr) → 2 ile temsil edilir (hata mesajları).

Yönlendirme ile standart giriş/çıkış değiştirilebilir.


Bazı durumlarda komutların çıktısının ekranda görüntülenmesi yerine bir dosyaya kaydedilmesi veya başka bir yere gerekebilir (> ve  >>). 

\> → Çıktıyı bir dosyaya yazar (dosyanın içeriğini siler, üzerine yazar).
```bash
ls > cikti.txt # cikti txtye yönlendir ls yi yoksa oluştur.
```
\>> → Çıktıyı dosyanın sonuna ekler (var olan içeriği silmez).
```bash
echo "Merhaba" >> cikti2.txt
```
Birden çok dosya içeriğini birleştirerek yeni bir dosyaya yönlendirmek de mümkündür. 
```bash
cat cikti.txt cikti2.txt >> yenicikti.txt
```

Ya da bir komut girdisinin klavyeden değil de herhangi bir başka birimden alınması istenebilir (<).

komut < dosya
```bash
wc -l < metin.txt
```
##  REGEX

Düzenli deyimler (Regular Expressions - Regex), metin içinde belirli kalıpları aramak, eşleştirmek ve manipüle etmek için kullanılan güçlü bir araçtır.

<img src="./assets/REGEX.PNG" alt="alt yazı" width="800">


Satır başında a karakteriyle başlayıp devam eden sözcükler: ^a

Satır başında 3 adet z karakteri bulunan sözcükler: ^zzz veya ^z\{3\}

Satır başında en az 2 adet k karakteri bulunan sözcükler: ^k\{2,\}

Satır sonunda y karakteri ile sonlanan sözcükler: y$
f
Satır başında K karakteri ile başlayıp, satır sonunda M ile biten sözcükler: ^K.*M$

Yanlış yazılmış olma ihtimalini göz önüne alarak hem tren ve hem de tiren kelimelerini yakalayacak düzenli deyim: ti?ren

## grep (global regular expressions print) Komutu

grep         <Düzenli Deyim>         < Dosya Adı>


grep komutu düzenli deyim olarak  [], ., ^, $ ve * karakterlerini kullanır .
Diğer düzenli deyim karakterlerini de (örneğin +, ?, |, {}) kabul eden aramalar yaptırmak için 3 farklı yol vardır:
1) grep komutundan faydalanıldığı durumlarda desteklenmeyen sembollerin önünde \ karakterini kullanmak,
2) grep komutunu ile -E seçeneği ile birlikte kullanmak,
3) egrep komutunu kullanmak. (Extended Regular Expression)

```bash
grep "^A" notlar.txt # ^A → satır başı A ile başlayan satırları bulur

```

Grep komutu büyük küçük harfe duyarlıdır. 


* küçük büyük harf duyarlılığını ortadan kaldırmak için -i  seçeneği
```bash
grep -i "linux" dosya.txt

```
Dosya.txt içinde linux, Linux, LINUX vb. tüm varyasyonları bulacaktır.

* -v kullanılırsa eşleşmeyen satırları gösterir.
```bash

grep -v "error" log.txt
```
➡ log.txt içindeki "error" geçmeyen satırları listeler.

* -n veya --line-number Eşleşen satırların satır numaralarını da gösterir.
```bash

grep -n "main" program.c
```
➡ program.c dosyasında "main" geçen satırları, satır numarası ile birlikte yazar.
* -o veya --only-matching Satırın tamamını değil, sadece eşleşen kısmı yazdırır.
```bash
grep -o "error" log.txt
```
➡ log.txt içindeki sadece "error" kelimesini gösterir.

*  -c veya --count Eşleşen satırların sayısını gösterir.
```bash
grep -c "error" log.txt
```
➡ log.txt dosyasında "error" geçen kaç satır olduğunu gösterir.


## cut Komutu
```bash
cut [SEÇENEKLER] [DOSYA]
```
Dosya veya dosyalardaki sütunları görüntüler. -d (--delimiter) ile sütun ayıracı, -f (--fields) ile sütun numarası belirtilir.
```bash
Virgülle ayrılmış dosyada 1. ve 3. alanları al
cut -d',' -f1,3 data.csv

İki nokta üst üste ile ayrılmış dosyada 1. alanı al
cut -d':' -f1 /etc/passwd
```
```bash
# 2. alanı al
cut -d',' -f2 file.csv

# 1, 3 ve 5. alanları al
cut -d',' -f1,3,5 file.csv

# 2'den 4'e kadar olan alanları al
cut -d',' -f2-4 file.csv

# 3. alandan sonraki tüm alanları al
cut -d',' -f3- file.csv
```
```bash

# Her satırın ilk 5 karakterini al
cut -c1-5 file.txt

# 3. karakterden 10. karaktere kadar
cut -c3-10 file.txt

# 1, 3, 5. karakterleri al
cut -c1,3,5 file.txt
```


## sort Komutu
```bash

sort [SEÇENEKLER] [DOSYA...]
```

sort komutu giriş dosyasının satırlarını alfabetik veya nümerik olarak sıralar.

Sıralamanın ASCII tablosu kullanılarak  olarak gerçekleştirilmesini istiyorsanız sort komutunu çalıştırmadan önce komut satırında ```export LC_ALL=C  ```çalıştırmalısınız. 

```bash

# Alfabetik ters sıralama (Z'den A'ya)
sort -r names.txt


# Sayıları sayısal değere göre sıralar
sort -n file.txt


# 2. alana göre sırala
sort -k2 data.txt

```

## find Komutu 

```bash
find [ARAMA_YOLU] [SEÇENEKLER] [İFADE] [EYLEM]
```
find dosya/dizin arama işlemlerini gerçekleştirir. Wildcards kullanıyoruz.


```bash
# Geçerli dizinde tüm dosyaları listele
find .

# /home dizininde tüm dosyaları ara
find /home

# Belirli isimde dosya ara
find . -name "test.txt"

# Birden fazla dizinde ara
find /home /var /tmp -name "*.log"


# Tam isim eşleşmesi (büyük/küçük harf duyarlı)
find . -name "config.txt"

# Büyük/küçük harf duyarsız
find . -iname "CONFIG.TXT"

# Wildcard kullanımı
find . -name "*.txt"


# Tam olarak 100 byte olan dosyalar
find . -size 100

# Çalıştırınca, bulunduğun klasörün içinde veya alt dizinlerde "Desktop" adında klasör varsa, yolunu ekrana yazacaktır.

find   .   -type  f  -name  deneme.txt

find   .   -type  d  -name  Desktop

```

## wc (word count) Komutu

wc (word count) komutu, metin dosyalarındaki satır, kelime ve karakter sayısını sayar.
```bash
wc dosya.txt
```
Standart Çıktı Formatı

satır_sayısı  kelime_sayısı  karakter_sayısı  dosya_adı

-l (lines) - Sadece satır sayısı
```bash

wc -l dosya.txt
# Çıktı: 25 dosya.txt
```


-w (words) - Sadece kelime sayısı
```bash
wc -w dosya.txt
# Çıktı: 150 dosya.txt
```
-c (characters) - Sadece karakter sayısı

```bash
wc -c dosya.txt
```

Boru (Pipe) İşlemleri

Bir komutun çıktısını başka bir komuta yönlendirmek . 

Hatırlatma , Komut çıktısının bir dosyaya yönlendirilmesinde > ve >>  kullanılıyordu.

Bu işlem için  ( | )  kullanılır.

```bash
komut1 | komut2 | komut3
```
Örnekler
```bash
ls | grep "txt"

# Bulunduğun dizindeki dosyaları listeler, sonra içinde txt geçenleri filtreler.

cat dosya.txt | grep "error" | wc -l
# dosya.txt içinde "error" geçen satırların sayısını verir.


```



* wc -l deneme.txt

   16 deneme.txt

* wc -l < deneme.txt 

   16 

* cat deneme.txt | wc -l 

   16


Bu üç komut arasındaki fark girdi yöntemi ve çıktı formatındadır:

#### ilki için

Argüman olarak dosya verme

wc komutu dosyayı doğrudan açar

Çıktıda dosya adı da gösterilir
#### ikinci için

Input redirection (girdi yönlendirme)

Shell dosyayı açar ve içeriği wc'ye gönderir

wc komutu dosya adını bilmez

Sadece sayı gösterilir (dosya adı yok)


#### ücüncü için

Pipe kullanımı

cat dosyayı okur, wc pipe'dan veri alır

wc komutu dosya adını bilmez

Sadece sayı gösterilir (dosya adı yok)


| Komut                    | Çıktı | Dosya Adı | Girdi Yöntemi       | Performance |
|---------------------------|-------|-----------|-------------------|------------|
| `wc -l deneme.txt`        | 16    | ✅ Gösterir | Argüman           | En hızlı    |
| `wc -l < deneme.txt`      | 16    | ❌ Göstermez | Input Redirection | Hızlı       |
| `cat deneme.txt \| wc -l` | 16    | ❌ Göstermez | Pipe              | En yavaş    |


##  Editör (Metin Düzenleyicisi)


### vim

vim   deneme.cpp

Editör bu aşamada yeni bir dosya oluşturur.

Dosya mevcutsa içerik komut penceresine yansıtılır.

- Escape mod (Normal mod)

Çıkmak için Esc tuşu kullanılır.

- Insert mod (Düzenleme modu)

Escape mod

vim programından çıkmak için 			:q

Dosyadaki değişiklikleri kaydetmek için 		:w

Değişiklikleri kaydederek çıkmak için 		:wq

Değişiklikleri kaydetmeden çıkmak için 		:q!

İmlecin bulunduğu satırı kopyalamak için 	yy

:x 		Eğer dosyada herhangi bir değişiklik olduysa  			kaydet ve çık, aksi durumda sadece çık. (exit)

Kopyalanan karakter dizisini yapıştırmak için 	p	

/kelime	: İmlecin bulunduğu yerden itibaren istenilen kelimeyi arar.

?kelime	: İmlecin bulunduğu yerden itibaren geriye doğru  kelimeyi arar.

Kelimeyi aradıktan sonra aynı kelimenin geçtiği bir sonraki yeri bulmak için:

n			: Aynı yönde kelimeyi arar.

N			: Zıt yönde kelimeyi arar.

Satır numaralarını göstermek için:

:set nu
Satır numaralarını gizlemek için:

:set nonu

Ctrl+G ile ekranın alt tarafında bulunulan satır ve dosya hakkında bilgi alabilirsiniz.


Basitçe dosya açma:
vim dosyaAdi

İmleci belirtilen satırda konumlandırarak dosya açma:
vim +satirNo dosyaAdi

satirNo seçeneği boş bırakılırsa editör imlecin dosyada en son konumlandırıldığı satırda iken açılır.

Dosyayı imleci istenilen kelimenin geçtiği ilk satırda konumlandırarak açma:
vim +/kelime dosyaAdi


### nano

^ klavyedeki Ctrl tuşunu temsil eder.

^o tuş kombinasyonu dosyada yaptığınız değişiklikleri kaydetmek için kullanılır.

^x tuş kombinasyonu programdan çıkmak için kullanılır.

^g tuş kombinasyonu programın kullanımı ile ilgili bir yardım ekranı açar.


##  Kabuk Programlama


```bash
#!/bin/bash   # bash kabuğunun kullanılacağını söylüyoruz.Eğer belirtilmezse program üzerinde bulunulan kabuk tarafından çalıştırılır.
# Bu bir yorum satırı
echo "Merhaba Dünya!"
```
nano veya vim de açabildiğiniz gibi geditte de açabilirsiniz.
gedit = Linux'ta grafik tabanlı metin editörü (GNOME Text Editor)


gedit   deneme.sh

Merhaba.sh = açılacak/oluşturulacak dosya
Bu komut Merhaba.sh dosyasını gedit'te açar
Terminal bloke olur - gedit kapanana kadar yeni komut yazamazsınız

gedit   deneme.sh   &

Aynı işlemi yapar ama arka planda çalıştırır
& = komutu arka plan işi (background job) yapar
Terminal bloke olmaz - gedit açıkken de yeni komutlar yazabilirsiniz.


Daha sonra konsol penceresini açın ve dosyanıza chmod u+x komutuyla çalıştırma  izni veriniz.
 chmod     u+x     deneme.sh

 bu işlemden sonra aşağıdaki komutla çalıştırabilirsiniz.
 ```bash
 ./Merhaba.sh
 ```
çalıştırma hakkı vermeden çalıştırmak için
 ```bash
bash       Merhaba.sh
```
başka dizinde çalıştırma için
 ```bash
/home/bugor/scripts/deneme.sh
```

Değişkenler
 ```bash
 #Degisken tanımlarken atama ifadesinde boşluk olmamalıdır.
isim="Ahmet" 
yas=25
echo "Merhaba $isim, yaşınız $yas"
```

## Kabuk programlama klavyeden veri girme
 ```bash
#!/bin/bash
echo "Adınızı giriniz:" # -n seçeneği ile alt satıra gitmeyi engelle.echo -e seçeneği backslash escape karakterlerinin yorumlanmasını etkinleştirir 
read isim
echo "Merhaba $isim!"
```

## printf Komutu ile Ekrana Formatlı Veri Yazdırma

 ```bash
#!/bin/bash
# Format string ile
printf "Merhaba %s!\n" "Ahmet" # Çıktı Merhaba Ahmet!

# %d - Tam sayı (decimal)
printf "Yaş: %d\n" 25

printf "%f\n" 5  #  Çıktı: 5.000000

printf "There are %d customers with purchases over %d.\n" #  Çıktı:  50 20000 There are 50 customers with purchases over 20000.

printf "%10d\n" 11  #  %10d → sayıyı 10 karakterlik alan içinde sağa yasla.

printf "%-10d %-10d\n" 11 12  #  %-10d → sayıyı 10 karakterlik alan içinde sola yasla. çıktı: 11         12

printf "%10.5f\n" 5.3  # %10.5f → 10 karakterlik alanda, virgülden sonra 5 basamak göster.    5.30000
```


```bash
#locale
export LC_NUMERIC="en_US.UTF-8"
```
locale → sistemin dil, tarih, sayı, para birimi ayarlarını gösterir.

LC_NUMERIC → sayıların gösterim biçimini belirler.

Örneğin Türkçe locale’de ondalık ayırıcı , (virgül) olabilir.

en_US.UTF-8 yaptığında ondalık ayırıcı . (nokta) olur.

Yani:

LC_NUMERIC=tr_TR.UTF-8 → 5,30000

LC_NUMERIC=en_US.UTF-8 → 5.30000

## Aritmetik İşlemler
```bash

#!/bin/bash

# Temel işlemler
a=10
b=3

((toplam=a + b)) # 1. atama işlemi
fark=$((a - b)) # 3. atama işlemi
carpim=$((a * b))
let bolum=a/b;        # 3. atama işlemi
kalan=$((a % b))        # Mod (kalan)
us=$((a ** b))          # Üs alma

printf "Toplam: %d\n" $toplam      # 13
printf "Fark: %d\n" $fark          # 7
printf "Çarpım: %d\n" $carpim      # 30
printf "Bölüm: %d\n" $bolum        # 3
printf "Kalan: %d\n" $kalan        # 1
printf "Üs: %d\n" $us              # 1000
```


## bc Komutu (basic calculator)

| Komut | Çıktı | Açıklama |
|-------|-------|----------|
| `echo "57+43" \| bc` | `100` | Toplama işlemi yapar. |
| `echo "57-43" \| bc` | `14` | Çıkarma işlemi yapar. |
| `echo "57*43" \| bc` | `2451` | Çarpma işlemi yapar. |
| `echo "scale=25;57/43" \| bc` | `1.3255813953488372093023255` | `scale` → virgülden sonra kaç basamak gösterileceğini belirler. |
| `echo "scale=30;sqrt(2)" \| bc` | `1.414213562373095048801688724029` | `sqrt()` → karekök hesaplar. `scale` → basamak sayısı. |
| `echo "6^6^6" \| bc` | Çok büyük sayı | `^` → üs alma (power). |
| `echo "(7+6)*5" \| bc` | `65` | Normal matematik işlemleri, parantez önceliği geçerli. |
| `echo "obase=16;255" \| bc` | `FF` | `obase` → **çıktı tabanı**. Burada 255 → Hexadecimal (FF). |
| `echo "obase=2;12" \| bc` | `1100` | `obase=2` → binary çıktı. 12 → `1100`. |
| `echo "ibase=2;obase=A;10" \| bc` | `2` | `ibase` → **girdi tabanı**. `10` (binary) → 2 (onluk). |
| `echo "ibase=2;obase=A;10000001" \| bc` | `129` | `10000001` (binary) → 129 (onluk). |
| `echo "ibase=16;obase=A;FF" \| bc` | `255` | `FF` (hexadecimal) → 255 (onluk). |
| `sayi=5; echo "$sayi^2" \| bc` | `25` | Değişken kullanımı, üs alma. |
| `sayi=16; echo "$sayi/3" \| bc -l` | `5.33333333333333333333...` | `-l` → matematik kütüphanesi (ondalık işlemleri açar). |
| `a=22; b=7; echo "$a/($b-34)" \| bc -l` | `-.81481481481481481481` | Ondalık bölme, `-l` sayesinde küsuratlı sonuç. |


## test Komutu
test komutu bir karşılaştırma ifadesinin sonucunu öğrenmek.

Bash kabuğunda en son çalışan komutun sonucu $? ile öğrenilebilir. Eğer komut başarılı bir    0  sonucunu, diğer durumlarda sıfırdan farklı bir değeri geri döndürür.


```bash

#!/bin/bash

# test komutu ile
test 5 -eq 5
echo $?  # 0 (başarılı/doğru)

test 5 -eq 3  
echo $?  # 1 (başarısız/yanlış)

# Köşeli parantez ile (aynı işlev)
[ 5 -eq 5 ]
echo $?  # 0

[ 5 -eq 3 ]
echo $?  # 1
```

| Aritmetik İşlemler | Açıklama        | Karakter Dizileri | Açıklama       | Dosya/Dizin İşlemleri | Açıklama                  |
|--------------------|----------------|-------------------|----------------|------------------------|---------------------------|
| `-eq`              | Eşit Mi?       | `=`               | Eşit Mi?       | `-e`                   | Dosya/Dizin Mevcut Mu?    |
| `-ne`              | Eşit Değil Mi? | `!=`              | Eşit Değil Mi? | `-f`                   | Dosya Mı?                 |
| `-gt`              | Büyük Mü?      |                   |                | `-d`                   | Dizin Mi?                 |
| `-ge`              | Büyük Eşit Mi? |                   |                | `-r`                   | Dosya Okunabilir Mi?      |
| `-lt`              | Küçük Mü?      |                   |                | `-w`                   | Dosya Yazılabilir Mi?     |
| `-le`              | Küçük Eşit Mi? |                   |                | `-x`                   | Dosya Çalıştırılabilir Mi? |






Şartlı Deyimler (if, elif ve else)
```bash

if [ koşul ]; then
    # koşul doğruysa çalışacak komutlar
elif [ başka_koşul ]; then
    # ilk koşul yanlış, bu koşul doğruysa çalışır
else
    # yukarıdaki hiçbir koşul doğru değilse burası çalışır
fi

```

 Bir if deyiminde if komutu, ilk koşul, then ifadesi, koşul doğruysa çalışacak komut ve fi komutu zorunludur. 

```bash
#!/bin/bash
sayi=10

if [ $sayi -gt 0 ]; then
    echo "Sayı pozitiftir."
elif [ $sayi -lt 0 ]; then
    echo "Sayı negatiftir."
else
    echo "Sayı sıfırdır."
fi
```
```bash

if   test   $sayi   -gt   10  
if   [   $sayi   -gt    10   ]  

if   [   $sayi   \>  10   ]
if   [[   $sayi   >  10   ]]
```


Sayısal karşılaştırmalarda -gt (greater than) kullanmalısın:

✅ 1. if test $sayi -gt 10

✅ 2. if [ $sayi -gt 10 ]

Bunlar aynı şey (ikisi de POSIX standart).

-gt → sayısal karşılaştırma yapar.

Yani matematik mantığıyla 11 > 10 true, 9 > 10 false çıkar.

⚠️ 3. if [ $sayi \> 10 ]

Burada > operatörü kullanılmış → bu string (alfabetik) karşılaştırmadır.

\> yazman gerekiyor çünkü > tek başına yazarsan Bash bunu dosya yönlendirmesi (> file) sanıyor.

"9" \> "10" → TRUE döner çünkü ASCII’de '9' karakteri '1' karakterinden büyüktür.

⚠️ 4. if [[ $sayi > 10 ]]

Bu da string karşılaştırma yapar.

\ işareti gerekmez çünkü [[ ... ]] içinde yönlendirme sanılmaz.

Ama mantık yine alfabetik: "9" > "10" TRUE çıkar.

```bash
### Mantıksal VE

if   [   condition1   -a   condition2   ]

if   [   condition1   ]  &&  [   condition2   ]

if   [[   condition1   &&   condition2   ]]

### Mantıksal VEYA

if   [   condition1   -o   condition2   ]

if   [   condition1   ]  ||  [   condition2   ]

if   [[   condition1   ||   condition2   ]]
```

## Case yapısı
```bash

case değişken in
    pattern1)
        # komutlar
        ;;
    pattern2)
        # komutlar
        ;;
    *)
        # varsayılan durum
        ;;
esac
```
Örnek

```bash
#!/bin/bash
echo "Bir harf girin (a, b, c): "
read harf

case $harf in
    a)
        echo "A harfini seçtiniz"
        ;;
    b)
        echo "B harfini seçtiniz"
        ;;
    c)
        echo "C harfini seçtiniz"
        ;;
    *)
        echo "Geçersiz seçim!"
        ;;
esac
```

## Döngüler 

### While Döngüsü
```bash
while [ koşul ]; do
    # komutlar
done
```

### For Döngüsü
Kullanım 1 
```bash
for değişken in liste; do
    # komutlar
done
# Kullanım 2 
for((ifade1;ifade2;ifade3))
do
	komutlar 
done
```
Kullanım 2
```bash

for((ifade1;ifade2;ifade3))
do
	komutlar 
done

```
ifade1: Döngü değişkeninin ilk değeri

ifade2: Döngü koşulu

ifade3: Döngü değişkeninin güncellendiği aritmetik ifade

Örnek
```bash

for  i  in 1 2 3 4 5 6 7 8 9 10 

for((i=1;i<=10;i=i+1)) 

for  i  in {1..10}    	     # Brace Expansion

for  i  in `seq 1 10` 	     # sequence of numbers 

for  i  in $(seq 1 10) 	     # sequence of numbers

do
```
Hepsi aynı


## Kabuk Programı Argümanları

| Parametre | Açıklama                              |
| --------- | ------------------------------------- |
| `$0`      | Script adı                            |
| `$1`      | Kabuk programına aktarılan 1. argüman |
| `$2`      | Kabuk programına aktarılan 2. argüman  |
| `$#`      | Kaç argüman gönderildi                |
| `$@`      | Tüm argümanlar (her biri ayrı)        |
| `$*`      | Tüm argümanlar (tek string olarak)    |
| `$$`      | Script’in PID’si (process ID)         |
| `$?`      | Son çalıştırılan komutun çıkış durumu |

```bash
./Argumanlar.sh   Bugor   Etkingames
```

Kabuk Programinizin Adi       		:    ./Argumanlar.sh

Kabuk Programinizin Tum Argumanlari	:    Bugor     Etkingames     

Kabuk Programinizin Arguman Sayisi	:    2

Kabuk Programinizin 1. Argumani   	:    Bugor

Kabuk Programinizin 2. Argumani   	:    Etkingames


## Sayısı Bilinmeyen Argümanlara Erişim

```bash
#!/bin/bash

for i in "$@"
do
    echo "$i"
done

```
Açıklama:

\$* ve \$@ (tırnaksız kullanıldığında) aynı işlevi görür, tüm argümanları boşlukla ayırarak döner.

"$*" → Tüm argümanları tek bir string haline getirir.


Örn: 3 argüman (a b, c, d) verilirse:

"a b c d"

"$@" → Tüm argümanları ayrı ayrı stringler halinde korur.

Örn: 3 argüman (a b, c, d) verilirse:

"a b" "c" "d"

yani 3 ayrı argüman olur.

```bash
#!/bin/bash
for((i=1;i<=$#;i++))
do
	echo "${!i}";#echo "$i" ile fark?
done
```
${!i} ne demek?

${!i} → indirect expansion (dolaylı genişletme).

i değişkeninin değeri kaç ise, o pozisyondaki parametreyi çağırır.

$i ne demek?

$i → döngü değişkeninin değeri.

Yani i=1 ise $i → 1 yazdırır.


indirection örneği
```bash
i="hello"     # i = "hello"
hello="bye"   # hello = "bye"

echo "$i"     # -> hello
echo "${!i}"  # -> bye  (çünkü $i = "hello", yani aslında $hello okunuyor)
```

## Bir Dosyayı Satır Satır Okumak 
```bash
#!/bin/bash
cat $1|      
while read line
do
	echo "$line";	
done
```

```bash
#!/bin/bash
while read line
do
	echo "$line";	
done < $1      
```

## Kabuk Fonksiyonları

```bash
# Yöntem 1
function_name() {
    # komutlar
}

# Yöntem 2  
function function_name {
    # komutlar
}
```

```bash

#!/bin/bash

selamla() {
    echo "Merhaba $1" ## $1 ilk parametre
}

selamla "Deniz"
selamla "Ahmet"
```



Alt fonksiyon return komutu ile geriye bir değer döndürebilir ve bu değer alt fonksiyonun çağrıldığı yerde $? ile test edilebilir.

```bash

#!/bin/bash

kontrolEt() {
    if [ -f "$1" ]; then
        echo "Dosya bulundu: $1"
        return 0   # 0 → başarılı
    else
        echo "Dosya yok: $1"
        return 1   # 1 → hata
    fi
}

kontrolEt "deneme.txt"

if [ $? -eq 0 ]; then
    echo "İşlem başarılı."
else
    echo "İşlem başarısız."
fi

```
for i in $1/* yapısı, verilen dizin içindeki tüm dosya ve klasörleri tek tek dolaşmak için kullanılır.


## IFS (Input/Internal Field Separator)

Kabuk bu değişkeni kullanarak girdiyi nasıl parçalayacağını belirler.

Varsayılan olarak IFS şunları içerir:

Boşluk (space)

Tab (\t)

Yeni satır (\n)
```bash

# String'i kelimelere ayırma
text="apple banana cherry"
for word in $text; do
    echo "Kelime: $word"
done
# Çıktı:
# Kelime: apple
# Kelime: banana
# Kelime: cherry
```

```bash

# Virgülle ayrılmış değerler için IFS ayarlama
IFS=','
data="elma,armut,kiraz,üzüm"
for item in $data; do
    echo "Meyve: $item"
done

# IFS'yi eski haline getir
IFS=$' \t\n'
```

```bash

parse_ip() {
    local ip="192.168.1.100"
    local old_ifs="$IFS"
    IFS='.'
    
    set -- $ip  # Pozisyonel parametrelere ata
    echo "1. oktet: $1"
    echo "2. oktet: $2" 
    echo "3. oktet: $3"
    echo "4. oktet: $4"
    
    IFS="$old_ifs"
}
```

### DİZİLER 
 dizi indisi 0’dan başlar.

 dizilerin boyutları ile ilgili bir maksimum kısıtlaması yoktur.

```bash
 # Yöntem 1: Doğrudan atama
fruits[0]="elma"
fruits[1]="armut"
fruits[2]="kiraz"

# Yöntem 2: Parantez ile
fruits=("elma" "armut" "kiraz" "üzüm")

fruits=("elma" "armut" "kiraz")

#Boş dizi deklarasoyonu
$ fruits=();

# Tek elemana erişim
echo ${fruits[0]}    # elma 
echo $fruits         # elma
echo ${fruits}       # elma
echo ${fruits[1]}    # armut

# Tüm elemanlara erişim
echo ${fruits[@]}    # elma armut kiraz
echo ${fruits[*]}    # elma armut kiraz

# Son element
echo ${fruits[-1]}   # kiraz (Bash 4.3+)
```




```bash

Linux=("Debian" "Red Hat" "Ubuntu" "Suse" "Fedora")

for i in ${Linux[@]}; do
    echo $i  # Red ve hati ayrı olarak alır.
done

echo "BUDA İKİNCİ SATIR---------------------"

for i in "${Linux[@]}"; do #böyle aynen korunur.
    echo "$i"
done
```

# Dizi Dilimleme (Array Slicing)
```bash
numbers=(1 2 3 4 5 6 7 8 9 10)

# İndeks 2'den başlayarak 3 eleman
echo ${numbers[@]:2:3}    # 3 4 5

# İndeks 5'ten sonuna kadar
echo ${numbers[@]:5}      # 6 7 8 9 10

# Sondan 3 eleman
echo ${numbers[@]: -3}    # 8 9 10

$ Linux=("Debian"  "Red Hat"  "Ubuntu"  "Suse"  "Fedora");
$ echo ${Linux[2]:0:4}; #2. indeksteki elemanın ilk 4 karakteri çıktı Ubun

$ echo ${#Linux[@]}; ##Bir Dizinin Eleman Sayısı (Boyutu) 5

$ echo ${#Linux[2]}; #İndeks 2’de bulunan dizi elemanının boyutu  6

fruits=("elma" "armut")

# Sona ekleme
fruits+=("kiraz")
fruits[${#fruits[@]}]="üzüm"
$ Linux=("${Linux[@]}"  "Knoppix");

# Başa ekleme
$ Linux=("Kali Linux"   "${Linux[@]}"); 

# Belirli indekse ekleme
fruits[10]="muz"

# Dizinin İlk Elemanının Silinmesi
$ Linux=("${Linux[@]:1}");

$ Linux=("${Linux[@]:0:$((${#Linux[@]}-1))}");

# Bir Dizinin Aradan Bir Elemanının Silinmesi

pos=3; 
Linux=("${Linux[@]:0:$pos}"  "${Linux[@]:$((pos + 1))}"); 

# Bir Dizinin Kopyalanması
$ LinuxYedek=("${Linux[@]}");

fruits=("elma" "armut" "kiraz" "üzüm")

# Yöntem 1: Elemanları döngüde
for fruit in "${fruits[@]}"; do
    echo "Meyve: $fruit"
done

# Yöntem 2: İndeks ile döngü
for i in "${!fruits[@]}"; do
    echo "İndeks $i: ${fruits[i]}"
done

# Yöntem 3: C tarzı döngü
for ((i=0; i<${#fruits[@]}; i++)); do
    echo "Eleman $i: ${fruits[i]}"
done

```


## Karekter dizileri ile ilgili işlemler
Stringin uzunluğunun hesabı
```bash
# Yöntem 1
$ isim="Bugor";
$ echo ${#isim};
# Çıktı:5

# Yöntem 2

$ isim="Bugor";
$ echo "$isim" | wc -c 
# Çıktı:6 Çünkü echo komutu stringin sonuna otomatik olarak bir satır sonu karakteri (\n, newline) ekler.  echo -n "$isim" | wc -c 5 çıkar

echo `expr length "$isim"`
```
```bash


$ dosyaAdi="Uygulama1.sh";
$ uzantisizDosyaAdi=$(basename  $dosyaAdi  .sh); # 
$ echo $uzantisizDosyaAdi;
Uygulama1

$ dosyaAdi="Uygulama1";
$ uzantisizDosyaAdi=`basename  $dosyaAdi  .sh`;
$ echo $uzantisizDosyaAdi;
Uygulama1

```
Burada basename komutu kullanılıyor.

basename \<dosya> [uzanti] → bir dosya adını alır, varsa yol kısmını ve verdiğin uzantıyı atar, sadece saf dosya adını döndürür.



# Bir Dosyanın Uzantısının Ayrıştırılması
(Dosya Uzantısı Varsa Ama Uzantı Bilinmiyorsa)
(Dosya Adı Bir Tek Nokta Karakteri İçeriyorsa)
```bash

$ dosyaAdi="Uygulama1.sh";
$ uzantisizDosyaAdi=$(echo "$dosyaAdi"|cut  -d  '.'  -f  1);
$ dosyaUzantisi=`echo "$dosyaAdi"|cut  -d  '.'  -f  2`;
$ echo $uzantisizDosyaAdi;
Uygulama1
$ echo $dosyaUzantisi;
sh
```
# rev (reverse) Komutu
```bash

$ string1="ey edip adanada pide ye";
$ string2=$(echo "$string1"|rev);
$ echo $string2;
ey edip adanada pide ye
$ test "$string1"  =  "$string2";echo $?;#Palindrom Testi
0
```

Bir Dosyanın Uzantısının Ayrıştırılması
(Dosya Uzantısı Varsa Ama Uzantı Bilinmiyorsa)
(Dosya Adı Birden Fazla Nokta Karakteri İçeriyorsa) (1)


```bash

$ dosyaAdi="Uygulama1.sh.txt.jpeg";
$ uzantisizDosyaAdi=$(echo "$dosyaAdi"|rev);
$ echo $uzantisizDosyaAdi
gepj.txt.hs.1amalugyU
$ uzantisizDosyaAdi=$(echo "$dosyaAdi"|rev|cut -d '.' -f 2-);
$ echo $uzantisizDosyaAdi
txt.hs.1amalugyU
$ uzantisizDosyaAdi=$(echo "$dosyaAdi"|rev|cut -d '.' -f 2-|rev);
$ echo $uzantisizDosyaAdi
Uygulama1.sh.txt

```
