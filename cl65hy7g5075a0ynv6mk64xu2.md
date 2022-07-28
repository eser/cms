## laroux.js

DOM ve JavaScript ile hiçbir zaman sorunu olmamış biri olarak, jQuery hayatıma girdikten sonra ürettiğim frontend kodlarda belirli bir ivme kazandığımı düşünüyorum. jQuery ilk adımlarını atarken Prototype ve Mootools gibi şu günkü yaygınlıklarıyla karşılaştırıldığında daha popüler iki alternatife daha sahipti. Önce her browser’a göre farklı kod üretiminin önüne geçti jQuery. Kompleks DOM ağaçlarından kolayca sıyrılabildiğiniz bir taban oturtmuştu esnek plugin yapısıyla birlikte. Zamanla içerisinde tüm avantajlarının yanına bir de kolay kullanılabilir ajax çözümünü ekledi ve bugünkü popülerliğine ulaştı.

Internet Explorer’ın standartlara her geçen gün yaklaşmasıyla ve artık kullandığımız browserların sürüm numarasını bilmiyor oluşumuzla frontend development için bir takım şeylerin değişeceği yeni bir döneme girdik fark etmeden. Örneğin esas ismi Sizzle olan, jQuery’nin arkasındaki güç yani DOM objelerine CSS notasyonuyla ulaşmanızı sağlayan JavaScript kodu, yükünü CSS3 ve W3C standartlarıyla birlikte güçlenen browserlara bırakabiliyor.

jQuery ise 1.9 sürümüyle kullanıcılarına bazı alışkanlıkları bırakmaları gerektiği mesajı vererek bir çok fonksiyonunu “deprecated” olarak işaretledi. 2.0 sürümünü ise tamamiyle modern browserlara yönelik çıkartacağını, Internet Explorer’ın eski sürümlerine destek vermeyeceğini ima etti. Özet şu ki artık yepyeni bir jQuery olacak. jQuery 2.0 açıklaması yapmadan önce ben de ufak ufak kendi işlerimi halledebileceğim `laroux.js` isimli bir JavaScript kütüphanesi geliştirmiştim.

jQuery ile ilgili problemlerim:

*   jQuery’nin her browser’ı ve platformu’u destekleme çabası ile bloatware olmaya başlayan kodu yavaş bir frontend deneyimi yaşatabiliyor. Her browser v8 kullanmıyor ve jQuery 2.0 için dahi Windows 8 gibi JavaScript ile geliştirme yapılabilen platformlar kapsam içerisinde oysa ki yalnızca web’de frontend geliştirmesi için kullanıyorum jQuery’i.
*   Yine “2010’dan önce üretilmiş herhangi bir browser’ı desteklemek zorunda değilim” diye düşünen biri olarak modern bir browser’ın native fonksiyonları ile değil jQuery API’si ile konuşmak zorunda kalıyorum.
*   Sizzle’ın yaptığı işi modern browser’larda querySelector metodu üstlenebiliyor ama ben bu performansdan iki üç ekstra selector için feragat etmek zorunda kalıyorum.
*   JavaScript yazarken jQuery wrapper’ı içinden DOM objesine ulaşmak, DOM objesini jQuery wrapper’a döndürme hem performans kaybı hem de type karmaşası yaşıyorum.
*   jQuery idiot-proof tasarlandığı için ne yaptığını bilen bir kişi için başta CSS fonksiyonları olmak üzere inanılmaz fazla constraint kontrolüne sahip.

Bu nedenle herhangi bir wrapper olmaksızın native DOM’a erişebilen, ne yaptığını bilen, kodunu iyi test kişiler için uncompressed boyutu 364K yerine 36K olan, metodları single-responsibility’e göre tasarlanmış ve tamamiyle sonuca yönelik (ekstra düzeltme ve kontroller yok) modern browserlara hitap eden bir JavaScript kütüphanesi geliştirdim.

`laroux.js` [Kullanım Örnekleri](https://eserozvataf.github.io/laroux.js/), [Performans Testleri](https://eserozvataf.github.io/laroux.js/benchmarks.html) ve [Wiki Sayfaları](https://github.com/eserozvataf/laroux.js/wiki) ile indirip-kullanmaya elverişli durumda.

Her türlü soru, destek ve yardım için [GitHub Issues](https://github.com/eserozvataf/laroux.js/issues) ile bana ulaşabilirsiniz. Daha fazla detay için [laroux.js’nin proje sayfasını ziyaret edin](https://eserozvataf.github.io/laroux.js/).

*Originally published at* [*eser.ozvataf.com*](http://eser.ozvataf.com/laroux-js/) *on April 27, 2013.*