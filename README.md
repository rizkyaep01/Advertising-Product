# Optimizing Advertising Budgets
Dataset ini mencakup biaya iklan di berbagai platform (TV, Billboards, Google Ads, Media Sosial, Pemasaran Influencer, dan Pemasaran Afiliasi). Kolom ketujuh 'Product_Sold' mengukur jumlah unit produk yang terjual masing-masing. Dataset ini merupakan sumber daya berharga untuk menyelidiki dampak iklan terhadap penjualan produk. link untuk [dataset](https://www.kaggle.com/datasets/singhnavjot2062001/product-advertising-data).

Berikut adalah penjelasan singkat untuk setiap kolom:
- TV: Biaya periklanan yang dihabiskan untuk iklan di televisi.
- Billboards: Biaya periklanan yang dihabiskan untuk iklan di papan reklame.
- Google_Ads: Biaya periklanan yang dihabiskan untuk iklan melalui Google Ads.
- Social_Media: Biaya periklanan yang dihabiskan untuk iklan di platform media sosial.
- Influencer_Marketing: Biaya periklanan yang dihabiskan untuk kampanye pemasaran influencer.
- Affiliate_Marketing: Biaya periklanan yang dihabiskan untuk program pemasaran afiliasi.
- Product_Sold: Jumlah produk yang terjual.
## Overview
Project ini bertujuan untuk memaksimalkan penjualan produk dengan mengoptimalkan alokasi biaya iklan melalui pendekatan data science. Melalui analisis mendalam terhadap data, saya akan mengeksplorasi berbagai faktor yang mempengaruhi penjualan dalam kampanye periklanan. Dengan menggunakan teknik analisis data, seperti mencari koefisien antar variable yang relevan untuk mengembangkan strategi alokasi dana yang cerdas dan efektif. Hasil dari analisa ini diharapkan dapat memberikan panduan praktis bagi perusahaan dalam mengatur alokasi dana iklan secara optimal guna mencapai penjualan maksimal dalam anggaran yang tersedia.
## Business Questions
- Apakah alokasi biaya iklan sudah efektif?
- Bagaimana cara mengoptimalkan alokasi biaya iklan agar mendapatkan penjualan yang maksimal?
## Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import statsmodels.api as sm

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import r2_score, mean_squared_error, mean_absolute_error
```
## Result Preview
terjadi perubahan yang signifikan dalam alokasi biaya iklan sebelum dan setelah dioptimalkan.

![alt text](https://github.com/rizkyaep01/Optimizing-Advertising-Budgets/blob/main/pict/9koef.png?raw=true)

- berdasarkan coefisiennya, Affiliate_marketing memberikan kontribusi terbesar terhadap penjualan produk
- berdasarkan coefisiennya, Influencer_marketing memberikan kontribusi terkecil terhadap penjualan produk
- dari data yang ada, sebelum di optimalkan alokasi biaya yang dikeluarkan relatif hampir merata, namun secara coefision setiap fitur berbeda. jelas alokasi biaya tidak efektif
