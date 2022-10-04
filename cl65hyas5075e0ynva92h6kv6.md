## Debian ile usb disk mount etmek

Linux’un dizin yapısı nedeniyle disklere birbirinden bağımsız bölgeler halinde değil, belirlediğiniz bir dizin üzerinden erişirsiniz. Bu nedenle önce disk’e ulaşacağımız dizini oluşturmakla başlamalıyız. Ardından erişeceğimiz disk üzerindeki dosya sistemine (NTFS, ext, v.s.) göre ilgili sürücüyü yüklememiz, ve bunu diski tanımlarken belirtmemiz gerekmektedir.

Adım adım anlatmak gerekirse:

Öncelikle sisteme bağlı hangi device’ın disk olduğunu öğrenmek için:

```sh
$ fdisk -l
```

komutunu çalıştıracağız.

```
Device Boot Start End Blocks Id System /dev/sde1 63 488392064 244196001 7 HPFS/NTFS/exFAT
```

Yukarıdakine benzer bir ekran çıktısı ile USB sürücümüzün sistem tarafından device ismini öğrendikten sonra (`/dev/sde1`), diskin dosya sistemine göre ilgili driver’ı yüklememiz gerekecek. Örneğimizde “HPFS/NTFS/exFAT” dosya sistemini açabilmek için “ntfs-3g” sürücüsünü kullanacağız. Hangi sürücünün hangi dosya sistemi ile ilişkili olduğunu internet üzerinde ufak bir araştırma ile bulabilirsiniz. ntfs-3g sürücüsünü kurmak için:

```sh
$ apt-get install ntfs-3g
```

komutunu çalıştırdıktan sonra disk’in ulaşılacağı dizini oluşturmak için `/media/` dizini altında yeni bir klasör oluşturmamız gerekecek. Bunun için de:

```sh
$ mkdir /media/usbdrive
```

komutu yeterli olacaktır. Bu noktada “mount” işlemi öncesi temel hazırlığımız tamamlanmış bulunmakta. Temel hazırlıktan sonra diski her mount etmek istediğimizde yalnızca aşağıdaki noktadan ilerlememiz mümkün olacaktır.

```sh
$ mount -t ntfs-3g /dev/sde1 /media/usbdrive
```

Yukarıdaki “mount” komutunda görebileceğiniz üzere şu ana kadar adımlarda kullandığımız/bulduğumuz üç parametre olan sürücü (ntfs-3g), device (`/dev/sde1`) ve dizini (`/media/usbdrive`) komutla birlikte kullanmaktayız. Ardından tek yapmamız gereken:

```sh
$ cd /media/usbdrive
```

komutu ile diskimizin bulunduğu dizine geçiş yapmak olacaktır.