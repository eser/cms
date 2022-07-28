## WPF formuna dinamik XAML kodu enjekte etme

XAML ile ilgili yaptığım bir araştırma esnasında dış bir kaynaktan gelen kodu XAML içerisinde nasıl çalıştıracağım konusunda bir kaç örnekle karşılaştım. Eğer özellikle banner rotation yapacaksanız, veya canlı bir feed’i tamamiyle dışarıdan almayı düşünüyorsanız eminim oldukça işe yarayacaktır.

Görüldüğü gibi, dış bir kaynaktan alınan/okunan string’i `XamlUtils.GetXamlObject` metodu ile XAML’e dönüştürebiliyoruz. Burada dikkat etmemiz gereken bu metoddan dönen objenin XAML’in root element’ine düzgün cast edilmesinin gerekliliği. (Örnekte root element’i Grid olarak ele aldım)

*Originally published at* [*eser.ozvataf.com*](http://eser.ozvataf.com/wpf-formuna-dinamik-xaml-kodu/) *on November 12, 2008.*