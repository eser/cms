## Windows’da UAC’i aşmak için AdminElevator

Günün en az 15 saati bilgisayar karşısında olan biri olarak masaüstü özelleştirmek, ev temizliği yapmak gibi temel bir ihtiyaç benim için. DOS kullandığım zamanlardan bu yana 30–40 Kilobyte’lık programların mutluluğun anahtarı olduğunu düşünen biri olarak, nette araştırıp bulduğum ufak utilityler ile bugünlerde de benim için vazgeçilmez.

Fakat her zaman tam olarak işinize yarayacak bir utility bulamıyorsunuz, işte bu noktada eğer biraz programlama yeteneğiniz varsa iş başa düşüyor. Yıllardır bir çok utility yazdım kendim için, şimdi onları paylaşma ve revize etme zamanı geldi diye düşünüyorum. Bu utility’lerden ilki UAC ile ilgili.

Windows Vista ile birlikte sonra biz yazılımcılar UAC’den en fazla çeken kesim olmuşuzdur heralde. Sürekli kullanılan IDE’ler, Console uygulamalarını önce bir kez açar, ardından yetkimizin yetmediğini fark edip tekrar aynı programı bu sefer “Administrator” olarak açarız.

Peki hep Administrator olarak çalıştırsak olmuyor mu? Oluyor. Ama sıradan bir kullanıcının erişemeyeceği bir biçimde bu özellik de Windows’un derinliklerinde, Registry’de saklı. Geliştirdiğim yazılım ise, kendisi aracılığıyla listeye eklediğiniz çalıştırılabilir dosyalarını çalışmadan önce sizden Administrator yetkisi istiyor.

Böylece siz de en basitinden Command Prompt açmak için Search’e “cmd” yazıp, ardından sağ tıklayıp Run as Administrator demek yerine direkt Start->Run (Win+R kısayolu ile) aracılıyla “cmd” yazıp Admin olarak Command Prompt’u kullanabiliyorsunuz. Ayrıca daha önce eklediğiniz programı işiniz bittiğinde listeden kaldırabilirsiniz.

Programın C# kaynak kodlarına GitHub üzerinden ulaşabilirsiniz: [https://github.com/eserozvataf/adminelevator](https://github.com/eserozvataf/adminelevator)

*Originally published at* [*eser.ozvataf.com*](http://eser.ozvataf.com/windowsda-uac-i-asmak-icin-adminelevator/) *on November 30, 2011.*