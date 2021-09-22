---
layout: post
title:  "Set ile Top N ve Others Yönetimi"
language: tr
date:   2021-09-21
author: Tayip
categories: [Tableau]
excerpt: "Set ile Top n ve Others Yönetimi"
image: "assets/images/to5andothers.png" 
tags: [Tableau, Desktop, Top n, Others, ]
beforetoc: "Set ile Top n ve Others Yönetimi"
toc: false
youtube: https://www.youtube.com/embed/iJn15LFyENM
---
## Set ile Top n ve Others Yönetimi

Selamlar. Bu yazımda Tableau Desktopda Set ile Top n ve Others Yönetimini anlatacağım.

Bu konuyu Tableau Sample - **SuperStore** datası üzerinden anlatacağım. 

Product hiyerarşisi içerisinde bulunan Sub-category verisini rowsa bu veriye ait Sales verisinide columns'a ekliyoruz.

![sertifika ayarı](/assets/images/top-others-1.png)

Ardından Sub-category verisine sağ tıklayıp **Create>Set** ile yeni bir set oluşturuyoruz. Setler içerisine aldığı veriyi **in** bu veriler dışında kalanları ise **out** olarak gruplandırır. Oluşturulan setin özelliklerinde **Use All** diyerek içerisindeki verinin tamamını dahil ediyoruz. Bu şekilde 'in' kısmında Sub-category verisine ait tüm bilgiler alıyor. Ardında aynı pencere üstte bulunan **TOP** sekmesine gelerek burada 'in' içerisine almak istediğim verilerin Top 5'ini alıyoruz. Grafiğim satış verisiyle beslendiği için **By Field** seçeneğinde Sales verisinin Top 5 'ini alıyorum. Bu işlemle maksimum satış değeri olan 5 Sub-category'i 'in' kalanları ise 'out' grubuna almış oluyoruz.

![sertifika ayarı](/assets/images/top-others-2.png)

Oluşturduğunuz Set'i Rows'a sürükleyerek oluşturduğunuz işleme ulaşabilirsiniz.

![sertifika ayarı](/assets/images/top-others-3.png)

Şimdi Bir calculation oluşturuyoruz. İsmine Top 5 and Others diyorum. İçerisine aşağıdaki kodu ekliyoruz. İf şartına oluşturduğumuz seti ekliyoruz. Bu şekilde 'in' grubuna ait verilerde işlem yapar. Başına 'NOT' ekleyerek 'out' grubu için çalışması da sağlanabilir. 'in' grubu için değerlerde Sub-category verisini else de ise 'Others' diyerek kalanları tek bir grup haline getiriyoruz.

>IF [Sub-Category Set] THEN [Sub-Category]
ELSE 'Others' END 

![sertifika ayarı](/assets/images/top-others-4.png)

Oluşturduğumuz Top 5 and Others calculationunu rows da bulunan Sub-category'nin üzerine sürekleyip bırakıyoruz. Rowsda bulunan sete sağ tıklayıp **Show Header** diyerek verisini ekranda gizliyoruz. Artık Sub-category verisi Top 5 ve Others olarak gruplanmış şekilde servis edilebilir.

![sertifika ayarı](/assets/images/top-others-5.png)

Aynı zamanda Bir parametre ile iki Others veya Sub-category isimleri olacak şekilde geçiş de yapılabilir. Bunun için bir parametre oluşturuyoruz. **Data Type** String seçip aşağıdaki sekmeden bu parametrenin bir liste olmasını seçiyoruz. Buraya Sub-category ve Others olacak şekilde 2 değer giriyorum. 

![sertifika ayarı](/assets/images/top-others-6.png)

Arından bir calculation daha oluşturuyorum. İsmine Top 5 and Others with Parameter diyorum. İçerisine aşağıdaki kodu ekliyorum. İf'in şart kısmına oluşturduğumuz parametrenin 'Others' olduğunda ne yapacağı şartını veriyorum ki Top 5 and Others calculationunu kullanabileyim. Else Kısmında ise Sub-category diyerek parametrede bu seçildiğinde gelecek veriyi yazıyorum.

>IF [Parameter 3]='Others' THEN [Top 5 and Others]
ELSE [Sub-Category] END

![sertifika ayarı](/assets/images/top-others-7.png)

Ardında yazdığım son calculationu rowsda Top 5 and Others'ın üzerine sürekleyip bırakıyoruz. Data penceresinde sol attan parametreye sağ tıklayıp **Show Parameter** diyerek ekranın sol tarafında parametreyi gösteriyorum. Artık parametremde Others seçili iken tek bir grup, Sub-category seçili iken tüm grupları görüyorum. Category'i  **Collorsa** ekleyip birazda görsellik katmayı ihmal etmeyelim :))

![sertifika ayarı](/assets/images/top-others-8.gif)