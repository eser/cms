## C# Type Casting

Bir çok kişi type’lar arasındaki cast işlemleri için C-tabanli `(Type)Variable` dizilimini kullanmakta.

Bilindiği üzere, .NET CLR type casting işlemleri için aynı zamanda `Variable as Type` dizilimine de sahip. Genel tanıma göre bu dizilimin avantajları olarak okunabilirlik ve casting esnasında Exception oluşturmak yerine null döndürmesini sayabiliriz.

Microsoft Code Analysis’in tavsiyelerini dikkate almaya başlayana dek benim de konu ile ilgili bilgim arada yalnız davranış farklılığı olduğu yönündeydi. Oysa ki .NET klasik type casting dizilimini kullandığımızda aynı tipi birden fazla kez dönüştürüyormuş. Microsoft’un önerisi ise `Variable as Type` dizilimi ile performans arttırarak ve bu double-check’den kurtulmamız yönünde.

Durum böyle olunca ister istemez kendime sormaya başladım, Microsoft Managed Code’u inşa ederken sistemler büyüdükçe karşılaşılan escape karakterleri, sql injection gibi mevzularda daha akıllı davranacak diye pazarlamıyor muydu? Code Analysis’in bu noktada kullanıcıya output vermesi beni ikilemde bırakıyor. Dilerim Microsoft da bunları göz önünde bulunduruyordur.

Her neyse, ekstra referans olarak ufak bir araştırma sonrasında [.NET BLOG isimli bir blog’da iki type casting dizilimi için performans karşılaştırması](http://www.dotnet-blog.com/index.php/2007/06/28/the-c-as-operator/)na ulaştım. Aynı zamanda MSDN’de [How to: Safely Cast by Using as and is Operators](http://msdn.microsoft.com/en-us/library/cc488006.aspx) isimli bir makale bulunmakta.