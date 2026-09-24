# ML End-to-End: Store Sales Forecasting

## Problem
Corporación Favorita (Ekvador merkezli bir market zinciri) için her
mağaza-ürün ailesi kombinasyonunda günlük satış miktarını tahmin etmek
(zaman serisi tahminleme / time series forecasting).

## Kapsam
- 54 mağaza × 33 ürün ailesi = 1782 ayrı seri
- Daraltma yok, tam kapsam

## Başarı kriteri
- Birincil metrik: **RMSLE** (Root Mean Squared Logarithmic Error) —
  yarışmanın resmi metriği, düşük değer daha iyi
- Baseline karşılaştırması: naif tahmin (geçen haftanın aynı günü) —
  ilk modelin bu baseline'ı ne kadar geçtiğini takip edeceğim

## Veri
- `train.csv` — geçmiş satışlar (tarih, mağaza, ürün ailesi, satış, promosyon)
- `test.csv` — tahmin edilecek dönem
- `stores.csv` — mağaza metadata (şehir, tip, cluster)
- `oil.csv` — günlük petrol fiyatı (Ekvador ekonomisi petrole bağımlı, dış değişken)
- `holidays_events.csv` — tatil/özel gün takvimi
- `transactions.csv` — mağaza başına günlük işlem sayısı

## Yol haritası
- Hf1: EDA, feature engineering, model seçimi/değerlendirme
- Hf4: PyTorch ile deneme, uçtan uca hat, deploy