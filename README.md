# recommendation-issues


## Association Rule Based Recommender System

### İş problemi

Türkiye’nin en büyük online hizmet platformu olan Armut, hizmet verenler ile hizmet almak isteyenleri buluşturmaktadır. Bilgisayarın veya akıllı telefonunun üzerinden birkaç dokunuşla temizlik, tadilat, nakliyat gibi hizmetlere kolayca ulaşılmasını sağlamaktadır.

Hizmet alan kullanıcıları ve bu kullanıcıların almış oldukları servis ve kategorileri içeren veri setini kullanarak **Association Rule Learning** ile ürün tavsiye sistemi oluşturulmak istenmektedir.

### Veri Seti Hikayesi

Veri seti müşterilerin aldıkları servislerden ve bu servislerin kategorilerinden oluşmaktadır. Alınan her hizmetin tarih ve saat bilgisini içermektedir.

Değişkenler;

* UserId: Müşteri numarası
* ServiceId: Her kategoriye ait anonimleştirilmiş servislerdir. (Örnek : Temizlik kategorisi altında koltuk yıkama servisi)
* Bir ServiceId farklı kategoriler altında bulanabilir ve farklı kategoriler altında farklı servisleri ifade eder.
* (Örnek: CategoryId’si 7 ServiceId’si 4 olan hizmet petek temizliği iken CategoryId’si 2 ServiceId’si 4 olan hizmet mobilya montaj)
* CategoryId: Anonimleştirilmiş kategorilerdir. (Örnek : Temizlik, nakliyat, tadilat kategorisi)
* CreateDate: Hizmetin satın alındığı tarih

## Hybrid Recommendation System

### İş problemi

ID'si verilen kullanıcı için item-based ve user-based recommender yöntemlerini kullanarak 10 film önerisi yapınız.

### Veri Seti Hikayesi

Veri seti, bir film tavsiye hizmeti olan MovieLens tarafından sağlanmıştır. İçerisinde filmler ile birlikte bu filmlere yapılan derecelendirme puanlarını barındırmaktadır. 27.278 filmde 2.000.0263 derecelendirme içermektedir. Bu veri seti ise 17 Ekim 2016 tarihinde oluşturulmuştur. 138.493 kullanıcı ve 09 Ocak 1995 ile 31 Mart 2015 tarihleri arasında verileri içermektedir. Kullanıcılar rastgele seçilmiştir. Seçilen tüm kullanıcıların en az 20 filme oy verdiği bilgisi mevcuttur.

#### movie.csv

27278 Gözlem;

* movieId:  Eşsiz film numarası.
* title: Film adı
* genres: Tür

#### rating.csv

20000263 Gözlem;

userid: Eşsiz kullanıcı numarası. (UniqueID)
movieId: Eşsiz film numarası. (UniqueID)
rating: Kullanıcı tarafından filme verilen puan
timestamp: Değerlendirme tarihi
