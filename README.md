Yaz ve Kış Meyveleri Sınıflandırması (Görüntü İşleme & Makine Öğrenmesi)

Bu proje, mevsimsel meyvelerin (yaz ve kış) makine öğrenmesi ve görüntü işleme teknikleriyle sınıflandırılmasını hedefleyen bir veri madenciliği çalışmasıdır. Çalışmada 2000’in üzerinde özgün meyve görseli kullanılmış ve üç farklı sınıflandırma algoritmasının performansı karşılaştırılmıştır.

📌 Proje Özeti

Veri Seti: Toplam 2323 adet özgün meyve görseli, Fatkun eklentisi kullanılarak toplanmıştır.

Kategoriler: "Yaz Meyvesi" ve "Kış Meyvesi"

Geliştirme Ortamı: Orange Data Mining Tool

Öznitelik Çıkarımı (Feature Extraction): Inception v3 modeli ile resimler 2048 boyutlu sayısal öznitelik vektörlerine dönüştürülmüştür.

Kullanılan Algoritmalar: k-En Yakın Komşu (kNN), Rastgele Orman (Random Forest), Yapay Sinir Ağları (Neural Network)

Doğrulama Yöntemi: 10-katlı Çapraz Doğrulama (10-fold Cross-Validation)

⚙️ Kullanılan Teknolojiler ve Araçlar

Orange Data Mining: Görsel programlama arayüzüne sahip, açık kaynaklı makine öğrenmesi ve veri madenciliği aracı

Image Analytics Eklentisi: Resim verilerini sayısal vektörlere dönüştürerek sınıflandırmaya hazır hale getiren Orange modülü

Fatkun Batch Download: Veri setinin internet üzerinden toplanması için kullanılan araç

📊 Makine Öğrenmesi Modelleri ve Performans Karşılaştırması
Algoritma	Doğruluk	AUC	F1-Skoru	Kesinlik	Duyarlılık
Neural Network	0.945 (%94,5)	0.986	0.945	0.945	0.945
kNN (k=1)	0.912 (%91,2)	0.971	0.912	0.913	0.912
Random Forest	0.835 (%83,5)	0.923	0.835	0.836	0.835
🔍 Sonuçların Değerlendirilmesi

En Başarılı Model: Neural Network, %94.5 doğruluk oranı ile en iyi performansı göstermiştir. Kış meyvelerini %93.6, yaz meyvelerini %95.4 oranında doğru tahmin etmiştir.

kNN: %91.2 doğruluk ile başarılı, ancak Neural Network'ün gerisindedir.

Random Forest: %83.5 doğruluk ile diğer modellere göre daha düşük performans göstermiştir; özellikle yaz meyvelerinde %17.8 hata payı gözlemlenmiştir.



🚨 Önemli Not – Veri Seti

Veri seti büyük olduğu için GitHub’a yüklenememiştir. Bu nedenle görselleri ayrı olarak Google Drive’dan indirmeniz gerekiyor. Workflow dosyası (meyvesiniflandirmasi_new.ows) veriler olmadan çalışmaz.

Adımlar:

Aşağıdaki linkten veri setini indirin:
🔗 Meyve Görselleri İndir – Google Drive
https://drive.google.com/file/d/1MYkVPmrjn1juCHxFwjOq9zFusedSLf5b/view?usp=sharing

İndirdiğiniz zip dosyasını açın. İçinde iki ana klasör olmalı:

yaz_meyveleri

kis_meyveleri

Bu klasörleri .ows dosyasının olduğu dizine yerleştirin. Örnek yapı:

/meyve_projesi/
   ├─ meyvesiniflandirmasi_new.ows
   ├─ yaz_meyveleri/
   └─ kis_meyveleri/

Orange’ı açın ve meyvesiniflandirmasi_new.ows dosyasını yükleyin.

Import Images widget’ına çift tıklayarak, veri setinizin bulunduğu ana klasörü seçin.

İş akışı tamamlandıktan sonra Test and Score veya Confusion Matrix widget’ları ile sonuçları inceleyin.

💡 Not: Workflow çalışırken görsellerin doğru klasörlerde olması çok önemli. Aksi takdirde model veri bulamayacağından hata verir.



🚀 Kurulum ve Kullanım

Orange Data Mining yazılımını bilgisayarınıza kurun.

Options -> Add-ons menüsünden Image Analytics eklentisini yükleyin.

Bu depoyu bilgisayarınıza klonlayın.

Meyve görsellerini ilgili klasörlere (yaz meyveleri, kış meyveleri) yerleştirin.

Orange uygulamasından meyvesiniflandirmasi_new.ows dosyasını açın.

Import Images widget’ına çift tıklayarak veri setinizin bulunduğu klasörü seçin.

İş akışı çalıştıktan sonra Test and Score veya Confusion Matrix widget’ları ile sonuçları inceleyin.
