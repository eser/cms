## Azer Koçulu, kik, left-pad ve NPM

Birkaç gün önce “11 satır internet’i kırdı” benzeri başlıklarla çıkan haber mutlaka sizlere de ulaşmıştır.

Konu internette bolca konuşuldu. Olayın tarafları olan [Azer Koçulu](http://medium.com/@azerbike/i-ve-just-liberated-my-modules-9045c06be67c), [Kik](https://medium.com/@mproberts/a-discussion-about-the-breaking-of-the-internet-3d4d2a83aa4d) ve [NPM](http://blog.npmjs.org/post/141577284765/kik-left-pad-and-npm) sırasıyla olay hakkında bizleri bilgilendirdiler. Ben hızlıca bir tekrar edeceğim, bunu yaparken de başlıklar kullanacağım ki okuyucu olarak konunun bildiğiniz kısımlarını hızlıca geçebilirsiniz.

### NPM Nedir?

NPM genellikle JavaScript’de oluşturulmuş projeler ve kütüphaneler için bir liman. İnsanlar/organizasyonlar kodlarını NPM’e bir isim altında gönderebiliyorlar. Ve NPM’in bünyesindeki projeler birbirlerine referans göstererek daha önce üretilmiş bir kodu tekrar yazmak yerine tekrar kullanarak zamandan tasarruf ediyorlar.

Bu kadar yüzeysel geçtiğime bakmayın, o ufak kodlar zaman geçtikçe, standartlar geliştikçe kendi ufak ölçeğinde sürekli güncellenerek diğer projeleri de mikro düzeyde sağlam tutmak gibi faydalar sağlıyor.

Bu zaman zaman ufak, zaman zaman kullanan projenin kendisinden büyük paketleri genellikle açık kaynak gönüllüsü insanlar NPM ve benzeri platformlarda paylaşıyorlar. Evet, birileri mesailerinden, sevdikleri ile geçirebileceği zamandan arttırıp insanlık için çalışıyor.

### Olay

Azer Koçulu NPM’de [274 adet](https://gist.githubusercontent.com/azer/db27417ee84b5f34a6ea/raw/50ab7ef26dbde2d4ea52318a3590af78b2a21162/gistfile1.txt) paketi bulunan bir geliştirici.

Bunlardan bir tanesi de [kik](https://github.com/starters/kik). Kik komut satırınca “kik” yazarak yeni proje oluşturmanızı sağlıyor. Ve bildiğim/anladığım kadarıyla “kick”, “kickstart” gibi bir anlama sahip.

Benim NPM’de komut satırından çalışan 1 adet paketim bulunuyor. Onun da ismi “sey”, o da üç harfli. Nasıl dosya listesi aldığınız komut “ls” veya “dir” ise komut satırı kullanırken kısa ve akılda kalabilecek bir isim koymaya özen gösteriyorsunuz.

Muhtemelen aynı motivasyonlarla ismini belirlemiş “kik” isimli bir mesajlaşma programı var. Azer Koçulu’dan kendi “kik” isimli projelerini başka bir yere taşımasını, “kik” ismini de kendilerine bırakmasını istiyorlar. Neden olarak da “kendi kullanıcılarının kafalarının karışabileceğini” öne sürüyorlar.

Azer Koçulu’nun “üzgünüm, ben açık kaynak bir proje yürütüyorum” diyerek tekliflerini reddetmesiyle birlikte mesajlaşma programı’nın sahibi firma patent avukatlarını Azer Koçulu’nun üzerine salacaklarını, kapısının çalınacağını, bu tarz hesaplarının ele geçirileceğini ve kaybedeceğini söyleyerek tehdit ediyor. Mesajın sonuna da “avukatları karıştırmadan bu işi halledelim, bir tazminat belirlesek de ismi değiştirsen?” anlamında bir şeyler ekliyor.

Azer Koçulu’nun yanıtı “bir daha beni rahatsız etmeyin” oluyor. Bu noktadan sonra işler daha da çirkinleşiyor fakat aradaki kısımları hızlıca geçersek firma “avukatlar gerçekten karışsın istemiyoruz” diyerek arabuluculuk yapılması için NPM’i devreye sokuyor.

NPM’in kararı “evet bizce kullanıcılar kik yazdıklarında mesajlaşma programını bulabilmeliler” olunca Azer Koçulu durumu protesto etmek için NPM üzerindeki tüm paketlerini geri çekiyor.

Geri çekerken söylediği bir söz bence oldukça etkili “Bu durum NPM’in kurumların bireylerden daha güçlü olduğu bir özel mülk olduğunu idrak etmemi sağladı” diyor Azer Koçulu.

Bunun üzerine bir kelebek etkisi ortaya çıkıyor ve React, Babel gibi bir çok popüler paket işlemez hale geliyor. Sorun 2.5 saatlik bir süre içerisinde çözülüyor.

Twitter üzerinde Azer Koçulu’yu fırsatçılıkla suçlayan bazı görüşlere de denk geldim. Ben mümkün olduğunca bu konuyla ilgili görüşlerimi olay aktarımına yansıtmamaya çalışsam da, şu noktayı eklemeden geçmek istemiyorum. İstatistik olarak düşünürseniz, dünyada başlatılan start-up sayısı ve projelere koyulan isim sayısının birbirine denk gelmesi oldukça olağan bir durum. Kik ismi halihazırda bir konfeksiyon üreticisi, Kamu İhale Kurumu gibi organizasyonlar tarafından da paylaşılıyor.

### Sonrası

NPM bu olaydan dersler çıkartıyor. Artık paket geri çekmek o kadar da kolay olmayacak.

Projesi çalışmayanlar olaydan ders çıkartıyorlar. Artık mikro düzeyde bağımlılık/kütüphane kullanacakları zaman daha ince eleyip daha sık dokuyacaklar.

Azer Koçulu’nun görüşü ise “açık kaynak camiasının eninde sonunda tamamiyle özgür bir NPM alternatifi üreteceği” yönünde.

Bu yazıyı olayı gerek İngilizce takip edemeyenler için gerekse örnek teşkil eden bir konunun kaybolmaması için buraya eklemek istedim.

Yazıda yalnızca olayı ve tarafları anlattım. Fakat ilerleyen günlerde bu olaya bağlı olarak “açık kaynak” ve veri/kod mülkiyeti hakkında bir yazı yazmayı tasarlıyorum. Bu nedenle burada bir referans noktası olması gereksinimi duydum.

*Originally published at* [*eser.ozvataf.com*](http://eser.ozvataf.com/azer-koculu-kik-left-pad-ve-npm/) *on March 24, 2016.*