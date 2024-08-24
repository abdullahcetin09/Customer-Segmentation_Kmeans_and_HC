# Customer Segmentation Using RFM Analysis

## Proje Hakkında

Bu proje, bir e-ticaret perakende verisi kullanarak müşteri segmentasyonu yapmayı amaçlamaktadır. Müşterilerin davranışlarını anlamak ve onları segmente ederek daha hedefli pazarlama stratejileri geliştirmek amacıyla RFM (Recency, Frequency, Monetary) analizi uygulanmıştır. RFM analizi, müşteri ilişkilerini ve değerlerini değerlendirmek için yaygın olarak kullanılan bir tekniktir.

## Veri Kümesi

- **Kaynak**: Online Retail Dataset
- **Veri Seti Özellikleri**:
  - **InvoiceNo**: Fatura numarası, her bir işlemi temsil eder.
  - **StockCode**: Ürün kodu, her bir ürün için benzersizdir.
  - **Description**: Ürün açıklaması.
  - **Quantity**: Satılan ürün adedi.
  - **InvoiceDate**: Fatura tarihi.
  - **UnitPrice**: Ürün birim fiyatı.
  - **CustomerID**: Müşteri kimliği, her bir müşteri için benzersizdir.
  - **Country**: Müşterinin bulunduğu ülke.

## Analiz Adımları

1. **Veri Ön İşleme**:
   - Eksik verilerin çıkarılması.
   - İptal edilen siparişlerin (fatura numarası "C" ile başlayan) temizlenmesi.
   - Yeni değişkenler türetilmesi (Monetary değeri gibi).

2. **RFM Analizi**:
   - **Recency**: Müşterinin en son işlem yaptığı tarihten bugüne kadar geçen süre.
   - **Frequency**: Müşterinin işlem yapma sıklığı.
   - **Monetary**: Müşterinin harcadığı toplam miktar.

3. **Kümeleme Analizi**:
   - Müşteriler K-Means ve Hiyerarşik Kümeleme yöntemleriyle segmente edilmiştir.
   - En uygun küme sayısı, Silhouette Skoru ve Dirsek Yöntemi kullanılarak belirlenmiştir.
   - Müşterilerin RFM özelliklerine göre kümeler oluşturulmuş ve bu kümeler görselleştirilmiştir.

4. **Sonuçlar**:
   - Her bir müşteri için oluşturulan kümeler, pazarlama stratejilerinin belirlenmesinde kullanılabilir.
   - Farklı müşteri segmentlerinin davranışları, elde ettikleri değerler ve müşteri sadakati üzerine çıkarımlar yapılmıştır.

## Kullanılan Kütüphaneler

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `plotly`
- `sklearn`
- `scipy`

## Nasıl Çalıştırılır?

1. Projeyi yerel bilgisayarınıza klonlayın.
2. Gerekli kütüphaneleri yükleyin.
3. Jupyter Notebook veya herhangi bir Python IDE'de çalıştırın.

## Sonuçlar ve Çıkarımlar

Bu analiz, müşteri davranışlarını daha iyi anlamaya yardımcı olur ve pazarlama kampanyalarının daha hedefli bir şekilde yapılmasını sağlar. RFM analizi ve kümeleme yöntemleri, müşteri segmentlerini anlamada ve iş stratejilerini geliştirmede güçlü araçlardır.
