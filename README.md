💼 YatırımcıDostum - Akıllı Portföy Yöneticisi
Bu proje, kişisel finans yönetimi, döviz kuru takibi, kripto para analizi ve portföy yönetimi için geliştirilmiş kapsamlı bir masaüstü uygulamasıdır.

🚀 Özellikler
💰 Döviz ve Altın Takibi
Dolar/TL Kuru: Anlık döviz kuru bilgisi

Euro/TL Kuru: Anlık döviz kuru bilgisi

Gram Altın: Güncel gram altın fiyatı (Investing.com'dan)

📊 Portföy Yönetimi
PyQt5 Arayüz: Kullanıcı dostu grafiksel arayüz

Veritabanı Kaydı: MySQL ile portföy verilerini saklama

Portföy Görüntüleme: Kayıtlı verileri listeleme

📈 Borsa ve Kripto Analizi
Hisse Tahmini: 30 günlük veriyle linear regression tahmini

Bitcoin Analizi: Ortalama fiyat, en yüksek/düşük değerler, grafik

Ethereum Analizi: Detaylı fiyat analizi ve grafik

Doğal Gaz Analizi: Fiyat trendleri ve grafik

📑 Raporlama
PDF Raporları: Tüm grafikler PDF olarak kaydedilebilir

Zaman Damgası: Raporlara otomatik tarih ekleme

🛠️ Yardımcı Araçlar
Ekonomi Haberleri: Investing.com'a otomatik yönlendirme

Hata Loglama: Tüm hatalar dosyaya kaydedilir

📁 Gereksinimler
bash
pip install PyQt5 mysql-connector-python requests numpy pandas matplotlib reportlab selenium yfinance scikit-learn
🔧 Kurulum
Projeyi klonlayın

MySQL veritabanı oluşturun:

sql
CREATE DATABASE portfoy;
USE portfoy;
CREATE TABLE param (
    id INT AUTO_INCREMENT PRIMARY KEY,
    İsim VARCHAR(100),
    Dolar DECIMAL(10,2),
    Euro DECIMAL(10,2),
    Altın DECIMAL(10,2),
    TL DECIMAL(10,2),
    Zaman DATETIME
);
Kodda aşağıdaki alanları kendi bilgilerinizle güncelleyin:

MySQL bağlantı bilgileri

ExchangeRate-API key

Microsoft Edge WebDriver'ı yükleyin

Programı çalıştırın:

bash
python smart-portfolio-manager.py
📂 Dosya Yapısı
smart-portfolio-manager.py - Ana program dosyası

hata_dosyam.txt - Hata loglama dosyası

kişisel finans hakkı.png - Uygulama ikonu

*.png - Oluşturulan grafik dosyaları

*.pdf - Oluşturulan PDF raporları

📊 Kullanılan Veri Seti
Borsa analizi için Stock Market Dataset.csv dosyası kullanılmaktadır. Bu dosyada:

Tarih (Date)

Doğal gaz fiyatları (Natural_Gas_Price)

Bitcoin fiyatları (Bitcoin_Price)

Ethereum fiyatları (Ethereum_Price)

🎯 Kullanım
Program çalıştırıldığında ana menü karşınıza gelir:

text
************** YATIRIMCIDOSTUM Uygulamasına Hoşgeldiniz🥰 **************
Yapabilecekleriniz:
1=Dolar/TL Değeri💵
2=Euro/TL Değeri💶
3=Gram Altın Değeri🪙
4=Portföyünüzü Veritabanına Kaydetme📓
5=Portföy Görüntüleme🔎
6=Hisse Tahmin Etme (Temel Seviye)
7=Borsa Analiz📈
8=Ekonomi Haberleri📰
9=Sistemden Çıkış
📝 Portföy Kayıt Arayüzü
seçenekte açılan PyQt5 penceresinde:

İsim

Dolar miktarı

Euro miktarı

Çeyrek altın miktarı

TL miktarı
girilerek veritabanına kayıt yapılır.

📈 Analiz Özellikleri
Hisse Tahmini
Yahoo Finance'den 30 günlük veri çeker

Linear Regression ile gelecek gün tahmini yapar

RMSE hata oranı hesaplar

Bitcoin Analizi
Ortalama fiyat

En yüksek fiyat ve tarihi

En düşük fiyat ve tarihi

Son 30 gün grafiği

Ethereum Analizi
Ortalama fiyat

En yüksek/düşük değerler

Tüm zamanlar grafiği

Detaylı teknik açıklama

📄 PDF Raporları
Her grafik için:

PNG olarak kaydetme

PDF'ye dönüştürme

Açıklama metinleri

Otomatik tarih damgası

⚠️ Hata Yönetimi
Tüm hatalar hata_dosyam.txt dosyasına kaydedilir:

Hata açıklaması

Hata tarihi

Kullanıcıya uygun mesaj gösterimi

🔗 API ve Araçlar
ExchangeRate-API: Döviz kurları için

Yahoo Finance: Hisse verileri için

Investing.com: Altın fiyatı ve haberler için

Selenium: Web scraping için

MySQL: Veritabanı için

PyQt5: Grafiksel arayüz için

ReportLab: PDF oluşturma için

⚙️ Teknik Detaylar
Tahmin Modeli: Scikit-learn Linear Regression

Web Scraping: Selenium WebDriver

Veri İşleme: Pandas, Numpy

Grafikler: Matplotlib

Arayüz: PyQt5

PDF: ReportLab

Veritabanı: MySQL Connector
