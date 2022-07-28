## Document destekli PostgreSQL

Başlarda NoSQL olarak ismini duyuran “Document Database” teknolojileri bildiğimiz ilişkisel veritabanlarına oranla apayrı bir yaklaşım gerektirdiği için kullanım istatistiklerinde çok keskin sıçramalar oluşturamıyor olsa da, gün geçtikçe projelerde kendilerine daha fazla yer bulmaya başlıyorlar.

En popüler zamanlarını 1992’lerde yaşayan, klasik “şema” destekli relational database’lerin sonu yakın mı bilemeyiz. Fakat mevcut veritabanı çözümü üreten organizasyonların mevcut veya yeni ürünlerle yakınlarda değişimler geçireceklerinin sinyalleri bizlere ulaşmaya başladı bile.

Veri tipleri konusunda oldukça geniş bir yelpaze sunan (ayrıca benim favori DBMS’im) PostgreSQL halihazırdaki XML ve contrib olarak ulaşılabilecek hstore veri tiplerinin yanı sıra 9.2 sürümünden itibaren JSON desteği de sunacağını açıkladı.

[myNoSQL](http://nosql.mypopescu.com/post/47692111874/posgresql-as-a-schemaless-database) blog’undan aldığım özetle birlikte bu veri tiplerini karşılaştırmamız gerekirse:

**XML**

*   built-in type
*   can handle very large documents (2 GB)
*   XPath support
*   export functions
*   no indexing, except defining custom ones using expression index

**hstore**

*   hierarchical storage type
*   in contrib (not part of the core)
*   custom functions
*   GiST and GIN indexes
*   supports also expression indexes

**JSON**

*   built-in type starting with PostgreSQL 9.2
*   validates JSON
*   support expression indexing
*   nothing else besides a lot of feature scheduled for

PostgreSQL çalışanı olan Christophe Pettus’un hazırladığı ve MongoDB ile PostgreSQL’in document database olarak kullanımını karşılaştırdığı slide’larını [PostgreSQL Wiki’si üzerinden download](https://wiki.postgresql.org/images/b/b4/Pg-as-nosql-pgday-fosdem-2013.pdf) edebilirsiniz.

*Originally published at* [*eser.ozvataf.com*](http://eser.ozvataf.com/document-destekli-postgresql/) *on April 12, 2013.*