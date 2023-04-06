# Horspool_Algoritmasi

### Horspool algoritması algoritması Amacı ne için kullanıldığı/kullanılabileceği ve çalışma şekli aşağıdaki gibidir:
<br>

Horspool algoritması, metin içinde bir deseni aramak için kullanılan bir arama algoritmasıdır. Bu algoritma, desenin sağa doğru kaydırılmasıyla ve eşleşen karakterlerin sayısına dayanarak arama yapar.

Algoritmanın çalışma şekli şu şekildedir:

    1-Aranacak metin ve aranan desen belirlenir.

    2-Desenin her bir karakteri için bir kaydırma tablosu oluşturulur. Bu tablo, her bir karakterin desenin sonundan kaç karakter önce tekrar edeceğini gösterir. Eğer bir karakter desen içinde tekrar etmiyorsa, tablodaki değer, desen uzunluğu + 1 olarak atanır.

    3-Desenin başlangıç konumu, metnin başlangıcına yerleştirilir ve desenin son karakteri ile metindeki karakterler karşılaştırılır. Eşleşen bir karakter bulunursa, desenin bir önceki karakteriyle metindeki bir önceki karakter karşılaştırılır ve bu işlem desen tamamen eşleşene kadar devam eder.

    4-Desenin son karakteriyle eşleşen bir karakter bulunursa, desenin tamamının metindeki konumu kaydedilir. Ardından desen, kaydırma tablosundaki değer kadar sağa kaydırılır ve işlem tekrarlanır.

    5-Eşleşen bir desen bulunana kadar adım 3 ve 4 tekrarlanır. Eğer desen bulunamazsa, arama işlemi sonlandırılır.

Horspool algoritması, büyük metinlerde ve desenlerde hızlı arama işlemleri yapmak için kullanılabilir. Özellikle, DNA dizileri gibi uzun metinlerde arama yapmak için etkili bir yöntemdir. Ayrıca, sözcük işlemcilerinde ve düzenli ifadelerde kullanılan bir arama algoritmasıdır.
<br><br>

### Horspool algoritması Çalışma zamanı analizi ve En iyi, En Kötü, Ortalama sınırları açıklamalı olarak belirtilecektir. Sadece sınır belirtilmeyecektir, nasıl bulunduğu anlatılacaktır:

Horspool algoritmasının çalışma zamanı, desenin her bir karakteri için kaydırma tablosunun oluşturulması için O(m) ve desenin metin içinde aranması için O(n) olmak üzere toplamda O(m+n)'dir. Burada m desen uzunluğu, n ise metin uzunluğudur.

    1- En iyi durum, aranan desenin metinde ilk karakterde eşleştiği durumdur. Bu durumda, algoritmanın çalışma zamanı O(m) olacaktır.

    2-En kötü durum, aranan desenin metinde hiçbir yerde eşleşmediği durumdur. Bu durumda, algoritmanın çalışma zamanı O(mn)'dir. Ancak, kaydırma tablosu oluşturma aşamasında desendeki tekrar eden karakterlerin sayısı az ise, bu durumda kaydırma tablosu oluşturma aşaması da O(m) olacaktır.

    3-Ortalama durum, kaydırma tablosunun etkin kullanımı nedeniyle en kötü durumdan daha iyi performans sağlar. Desenin sık tekrar eden karakterlere sahip olduğu durumlarda daha etkili olabilir.

Horspool algoritması, boyutu büyük olan metinlerde ve desenlerde etkili bir şekilde arama yapabilen bir algoritmadır. Ancak, desendeki tekrar eden karakterlerin sayısı az ise, algoritmanın performansı düşük olabilir.
