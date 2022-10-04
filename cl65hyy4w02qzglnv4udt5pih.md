## C# APIleri oluştururken hangi List sınıfını kullanmalı?

Generic `List<T>` sınıfının yeni sınıf türetirken (inheritance) kullanılması ve kullanılsa dahi APIlerde expose edilmesi tavsiye edilmiyormuş. Hemen bir alıntı ile durumu özetleyeyim:

> *We don’t recommend using List in public APIs for two reasons.*

> 1\. List is not designed to be extended. i.e. you cannot override any members. This for example means that an object returning List from a property won’t be able to get notified when the collection is modified. Collection lets you overrides SetItem protected member to get “notified” when a new items is added or an existing item is changed.

> 2\. List has lots of members that are not relevant in many scenarios. We say that List is too “busy” for public object models. Imagine ListView.Items property returning List with all its richness. Now, look at the actual ListView.Items return type; it’s way simpler and similar to Collection or ReadOnlyCollection.

.NET Framework içerisinde `List<T>` örneği gibi genişlemeye müsait olarak tasarlanmayan, fakat gündelik kullanımı oldukça yaygın bir çok sınıf var. Konunun teknik bir gerekçesi var mı bilmiyorum, ama benzerlerinin çokluğu nedeniyle durumun bir tasarım kararı olduğu ortada.

Kaynak ve Yorumlar: [http://blogs.msdn.com/kcwalina/archive/2005/09/26/474010.aspx](http://blogs.msdn.com/kcwalina/archive/2005/09/26/474010.aspx)