# YMT5270 Final Sınav Projesi: H2O ile Veri Analizi ve Makine Öğrenmesi

## Öğrenci Bilgileri
- **Ad Soyad**: Mohammed Abduljalil Saeed Ahmed 
- **Öğrenci Numarası**: 231137132
- **E-posta**: www.mhmmdalmndoop@gmail.com

## Proje Özeti
> *This project is the final assignment for the YMT5270 - Yenilikçi Makine Öğrenme Ortamları course, where the goal is to leverage the H2O.ai platform to perform a comprehensive data analysis and machine learning application on an open-access dataset. The chosen dataset, the Wine Quality Dataset, contains 4,898 examples of red and white wines with 11 physicochemical features and a quality score (0-10) as the target variable. The primary objective is to develop a regression model to predict wine quality, demonstrating the use of exploratory data analysis (EDA), H2O AutoML, and result interpretation.*

## Veri Seti
### Veri Seti Bilgileri
- **Wine Quality Dataset**: 
- **Kaynak**: *(https://archive.ics.uci.edu/dataset/186/wine+quality)*
- **Veri Seti Boyutu**: *(örn. 3640 satır, 11 sütun)*

# Final Project: Wine Quality Prediction with H2O.ai

## Project Overview
This project is the final assignment for the YMT5270 - Yenilikçi Makine Öğrenme Ortamları course, where the goal is to leverage the H2O.ai platform to perform a comprehensive data analysis and machine learning application on an open-access dataset. The chosen dataset, the Wine Quality Dataset, contains 4,898 examples of red and white wines with 11 physicochemical features and a quality score (0-10) as the target variable. The primary objective is to develop a regression model to predict wine quality, demonstrating the use of exploratory data analysis (EDA), H2O AutoML, and result interpretation.

## Introduction
- **Dataset**: Wine Quality Dataset
- **Source**: https://archive.ics.uci.edu/dataset/186/wine+quality
- **License**: Public domain
- **Details**: The dataset includes 3,640 red wine and 1,258 white wine samples, each with 11 features such as fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol, alongside a quality score (0-10) as the target. A 'type' column was added to distinguish red and white wines.
- **Goal**: Utilize H2O.ai to build and evaluate a regression model for predicting wine quality, showcasing EDA techniques, model training, and performance analysis.
- **Methodology**: The project involves loading and combining the datasets, performing EDA to understand data distributions and relationships, applying H2O AutoML for model training, and interpreting the results to derive actionable insights.

### Öznitelik Açıklamaları
| Öznitelik Adı       | Veri Tipi  | Açıklama                                      | Örnek Değer |
|----------------------|------------|-----------------------------------------------|-------------|
| fixed acidity       | Sayısal    | The amount of fixed acids in the wine (g/dm³) | 7.4         |
| volatile acidity    | Sayısal    | The amount of volatile acids (g/dm³)          | 0.7         |
| citric acid         | Sayısal    | The concentration of citric acid (g/dm³)      | 0.0         |
| residual sugar      | Sayısal    | The sugar content remaining after fermentation (g/dm³) | 1.9   |
| chlorides           | Sayısal    | The salt content in the wine (g/dm³)          | 0.076       |
| free sulfur dioxide | Sayısal    | Free sulfur dioxide content (mg/dm³)          | 11.0        |
| total sulfur dioxide| Sayısal    | Total sulfur dioxide content (mg/dm³)         | 34.0        |
| density             | Sayısal    | The density of the wine (g/cm³)               | 0.9978      |
| pH                  | Sayısal    | The acidity level of the wine (pH scale)      | 3.51        |
| sulphates           | Sayısal    | The potassium sulphate content (g/dm³)        | 0.56        |
| alcohol             | Sayısal    | The alcohol percentage by volume (%)          | 9.4         |
| quality             | Sayısal    | The sensory quality score (0-10)              | 5           |
| type                | Kategorik  | The wine type (red or white)                  | "red"       |


## Keşifsel Veri Analizi (Explanatory Data Analysis - EDA)
### Temel İstatistikler
> *Veri setine ait temel istatistikleri (ortalama, medyan, standart sapma, vb.) buraya ekleyiniz. Orange'dan alınan ekran görüntüleri ile destekleyebilirsiniz.*

### Veri Ön İşleme
> *Veri setinize uyguladığınız ön işleme adımlarını detaylandırınız:*
> - *Eksik verilerin nasıl işlendiği*
> - *Aykırı değerlerin tespiti ve işlenmesi*
> - *Veri normalizasyonu/standardizasyonu*
> - *Kategorik verilerin kodlanması*
> - *Diğer ön işleme adımları*

### Görselleştirmeler
> *Her görselleştirme için kısa bir açıklama yazınız. Görselleri bu repoya yükleyip, markdown içinde referans verebilirsiniz.*

### Öznitelik İlişkileri
> *Öznitelikler arasındaki ilişkileri analiz ediniz. Korelasyon matrisi, scatter plot matrisi gibi görsellerle destekleyiniz.*

## Makine Öğrenmesi Uygulaması
### Kullanılan Yöntem
> *Veri setinize uyguladığınız makine öğrenmesi yöntemini (sınıflandırma, regresyon veya kümeleme) belirtiniz ve neden bu yöntemi seçtiğinizi açıklayınız.*

### Modeller ve Parametreler
> *Denediğiniz modelleri ve kullandığınız parametreleri açıklayınız. Orange'da yapılandırdığınız widget ayarlarını ekran görüntüleri ile destekleyebilirsiniz.*

### Model Değerlendirmesi
> *Uyguladığınız modelin performansını değerlendiriniz. Kullandığınız değerlendirme metriklerini açıklayınız.*

#### Metrikler
| Metrik | Değer |
|--------|-------|
| Örnek Metrik 1 | 0.85 |
| Örnek Metrik 2 | 0.78 |
| ... | ... |

### Sonuçların Yorumlanması
> *Elde ettiğiniz sonuçları detaylı bir şekilde yorumlayınız. Modelin güçlü ve zayıf yönleri nelerdir? Başka hangi modeller denenebilirdi?*

## Sonuç ve Öneriler
> *Projenizin genel bir değerlendirmesini yapınız. Elde ettiğiniz sonuçlar hakkında çıkarımlarınızı ve gelecek çalışmalar için önerilerinizi yazınız.*

## Kaynaklar
> *Proje boyunca yararlandığınız kaynakları (makaleler, web siteleri, videolar, vb.) buraya ekleyiniz.*

1. Kaynak 1
2. Kaynak 2
3. ...

## Ekler
### ipynb Proje Dosyası
> * proje dosyanızı (.ipynb) bu repoya yükleyiniz ve buradan referans veriniz.*

### Veri Seti Dosyası veya Bağlantısı
> *Kullandığınız veri setini bu repoya yükleyebilir veya bağlantısını burada paylaşabilirsiniz.*
>
> [Veri_Seti.csv](veri_seti.csv) veya [Veri Seti Bağlantısı](https://ornek-veri-seti-baglantisi.com)
