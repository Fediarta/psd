---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

#              BAB II
#           DATA UNDERSTANDING
### A.PENGUMPULAN DATA  

Proyek ini menggunakan NLP dan data awal berupa teks dari web yang diambil dari Website kemenkes [https://ayosehat.kemkes.go.id/topik-az].kemudiam diolah lagi menjadi csv(Comma-separated value) ,dengan tiga kolom yang berupa.kolom pertama kolom pertanyaan ,kedua kolom jawaban dan ketiga kolom kategori.


```{code-cell}
#import library
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/Fediarta/psd/refs/heads/gh-pages/PSDNEW.csv", low_memory = False, encoding='utf8')
df.head()
```


### B.Deskripsi Data

di dalam file csv berisikan 200 baris dan 3 kolom:

I. Pertanyaan : berisikan contoh pertanyaan yang kemungkinan ditannyakan.

II.Jawaban     : berisi jawaban yang sesuai dengan pertanyaan .

III.Kategori   : mengkategorikan jenis pertanyaan,masuk dalam kategori apa.

    
```{code-cell}
data = df[['Pertanyaan', 'Kategori']]
data.head()
```
    
```{code-cell}
df.dtypes
```

```{code-cell}
df.describe()
```

```{code-cell}
df.info()
```
dari 200 baris dan 3 kolom tidak ada data yang kosong.

