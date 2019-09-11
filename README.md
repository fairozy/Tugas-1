# Tugas-1
> Nama	:	Fairozy Hanif Darmawan
>
> NIM		:	170411100106





### **Tugas 1 Penambangan Data**

#### **Mean (Nilai Rata-Rata)**

Yang dimaksud mean atau nilai rata-rata adalah jumlah seluruh data dibagi dengan banyaknya data. Cara menghitung mean adalah dengan menggunakan rumus menghitung nilai rata-rata dari sekumpulan data sebagai berikut. 

![Rumus nilai rata-rata atau mean](http://ukurandansatuan.com/wp-content/uploads/2016/11/Rumus-menghitung-mean-atau-nilai-rata-rata-300x70p.gif)

***Code*** :

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Rata-rata Umur",df['Umur'].mean())
print("Rata-rata Tinggi Badan",df['Tinggi Badan'].mean())
print("Rata-rata Berat Badan",df['Berat Badan'].mean())
print("Rata-rata Ukuran Sepatu",df['Ukuran Sepatu'].mean())
```

***Output :***

```python
Rata-rata Umur 40.558232931726906
Rata-rata Tinggi Badan 164.86144578313252
Rata-rata Berat Badan 52.5722891566265
Rata-rata Ukuran Sepatu 41.48795180722892
```



#### **Median (Nilai Tengah)**

Median adalah nilai data yang letaknya di tengah dari data yang telah diurutkan dari nilai terkecil sampai nilai terbesar. Biasanya median diberi simbol Me.

*Cara Menghitung Median*
Pada data yang banyaknya ganjil maka ada satu data di tepat tengah data yang telah diurutkan. Jika banyaknya data ganjil, maka median adalah data yang letaknya tepat di tengah sekumpulan data yang telah diurutkan tersebut . 

#Misalkan median dari 11 data berikut: 21, 27, 23, 25, 21, 28, 24, 27, 26, 25, 21
Urutan data dari yang terkecil: 21, 21, 21, 23, 24, **25**, 25, 26, 27, 27, 28
Median adalah data yang di tengah urutan yaitu 25

Pada data yang banyaknya genap maka ada dua data di tepat tengah data yang telah diurutkan. Jika banyaknya data genap, maka median data adalah rata-rata kedua data yang letaknya tepat di tengah sekumpulan data yang telah diurutkan tersebut .

Misalkan median dari 12 data berikut: 24, 33, 47, 60, 30, 24, 25, 35, 49, 41, 52, 58,
Urutan data dari yang terkecil: 24, 24, 25, 30, 33, **35**, **41**, 47, 49, 52, 58, 60
Median adalah rata-rata dua data di tengah = (35+41)/2 = 76/2 = 38

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Median Umur"           ,df['Umur'].median())
print("Median Tinggi Badan"   ,df['Tinggi Badan'].median())
print("Median Berat Badan"    ,df['Berat Badan'].median())
print("Median Ukuran Sepatu"  ,df['Ukuran Sepatu'].median())
```

***Output :***

```python
Median Umur 41.0
Median Tinggi Badan 165.0
Median Berat Badan 53.0
Median Ukuran Sepatu 42.0
```



#### **Modus**

Modus adalah data yang paling sering muncul atau yang memiliki frekuensi terbanyak dari sekumpulan data. Biasanya modus diberi simbol Mo. Cara menentukan modus adalah dengan menghitung frekuensi semua data lalu memilih data yang frekuensi munculnya terbesar.

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df["Tinggi Badan"].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Modus Umur            ",df['Umur'].mode())
print("Modus Tinggi Badan    ",df['Tinggi Badan'].mode()) 
print("Modus Berat Badan     ",df['Berat Badan'].mode())
print("Modus Ukuran sepatu   ",df['Ukuran Sepatu'].mode())
```

***Output :***

```python
Modus Umur             0    34
1    51
2    54
dtype: int64
Modus Tinggi Badan     0    171
1    175
dtype: int64
Modus Berat Badan      0    47
dtype: int64
Modus Ukuran sepatu    0    40
dtype: int64
```



#### **Standar Deviasi**

Standar deviasi adalah nilai statistik yang digunakan untuk menentukan bagaimana sebaran data dalam sampel, dan seberapa dekat titik data individu ke mean – atau rata-rata – nilai sampel.

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Standar deviasi Umur          :",df['Umur'].std())
print("Standar deviasi Tinggi Badan  :",df['Tinggi Badan'].std())
print("Standar deviasi Berat Badan   :",df['Berat Badan'].std())
print("Standar deviasi Ukuran Sepatu :",df['Ukuran Sepatu'].std())
```

***Output :***

```python
Standar deviasi Umur          : 11.7003853179926
Standar deviasi Tinggi Badan  : 8.8269114480857
Standar deviasi Berat Badan   : 4.582772743309866
Standar deviasi Ukuran Sepatu : 1.1316088783711435
```



#### **Count**

Count adalah pencarian hasil akhir dari keseluruhan data

***Code :***

```
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe())
df["Tinggi Badan"].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("varian Umur          :",df['Umur'].count())
print("varian Tinggi Badan  :",df['Tinggi Badan'].count())
print("varian  Berat Badan  :",df['Berat Badan'].count())
print("varian Ukuran Sepatu :",df['Ukuran Sepatu'].count()
```

***Output :***

```python
varian Umur          : 499
varian Tinggi Badan  : 499
varian  Berat Badan  : 499
varian Ukuran Sepatu : 499
  
```



#### **Nilai Minimal**

Nilai minimal adalah nilai terkecial dalam data tersebut. 

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Min Umuran        :",df['Umur'].min())
print("Min Tinggi Badan  :",df['Tinggi Badan'].min())
print("Min Berat Badan   :",df['Berat Badan'].min())
print("Min Ukuran Sepatu :",df['Ukuran Sepatu'].min())
```

***Output :***

```python
Min Umuran        : 20
Min Tinggi Badan  : 150
Min Berat Badan   : 45
Min Ukuran Sepatu : 40
```



#### **Nilai Maximal**

Nilai maximal adalah nilai terbesar dalam data tersebut.

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Max Umur          :",df['Umur'].max())
print("Max Tinggi Badan  :",df['Tinggi Badan'].max())
print("Max Berat Badan   :",df['Berat Badan'].max())
print("Max Ukuran Sepatu :",df['Ukuran Sepatu'].max())
```

***Output :***

```python
Max Umur          : 60
Max Tinggi Badan  : 180
Max Berat Badan   : 60
Max Ukuran Sepatu : 43
```



#### **Kuartil**

Kuartil adalah data yang membagi posisi sekumpulan data yang telah diurutkan menjadi empat bagian. Dalam satu urutan data terdapat 3 kuartil yaitu kuartil bawah, kuartil tengah, dan kuartil atas. Cara menentukan kuartil adalah sebagai berikut.

- Kuartil bawah adalah data pada posisi 1/4 dari kumpulan data yang telah diurutkan. Kuartil bawah disimbolkan dengan Q1.
- Kuartil tengah adalah data pada posisi 2/4 dari kumpulan data yang telah diurutkan. Kuartil tengah sama dengan median. Kuartil tengah disimbolkan dengan Q2.
- Kuartil atas adalah data pada posisi 3/4 dari kumpulan data yang telah diurutkan. Kuartil atas disimbolkan dengan Q3.

Posisi ketiga kuartil ditentukan dari rumus berikut.

**Posisi Qi = i(n+1)/4**

i = indeks kuartil yaitu 1, 2, 3 dan n = banyaknya data

Misalkan kita akan menentukan kuartil bawah, tengah, dan kuartil atas dari 15 data berikut: 11, 24, 12, 15, 12, 18, 22, 25, 26, 27, 17, 22, 24, 19, 12.

Urutan data dari yang terkecil:
11, 12, 12, 12, 15, 17, 18, 19, 22, 22, 24, 24, 25, 26, 27
Posisi ketiga kuartil adalah sebagai berikut
Posisi Q1 = 1.(15+1)/4 = (16)/4 = 4 (data urutan ke 4)
Posisi Q2 = 2. (15+1)/4 = 2(16)/4 = 8 (data urutan ke 4)
Posisi Q3 = 3. (15+1)/4 = 3(16)/4 = 12 (data urutan ke 4)
Berdasarkan posisi kuartil pada urutan data maka dapat ditentukan ketiga kuartil
11, 12, 12, **12**, 15, 17, 18, **19**, 22, 22, 24, **24**, 25, 26, 27
Jadi :

- kuartil bawah adalah 12

- Kuartil tengah = median = 19

- Kuartil atas = 24

  

#### **Kemiringan kurva (Skewnes)**

Skew merupakan derajat ketidak simetrian (keasimetrian), atau dapat juga disefinisikan sebagai penyimpangan dari kesimetrian dari suatu distribusi.

***Code :***

```python
import pandas as dt
df=dt.read_csv("rozdata.csv")
df['Umur'].describe()
df['Tinggi Badan'].describe()
df['Berat Badan'].describe()
df['Ukuran Sepatu'].describe()
print("Skewness Umur          :",df['Umur'].skew())
print("Skewness Tinggi Badan  :",df['Tinggi Badan'].skew())
print("Skewness  Berat Badan  :",df['Berat Badan'].skew())
print("Skewness Ukuran Sepatu :",df['Ukuran Sepatu'].skew())
```

***Output :***

```python
Skewness Umur          : -0.07073065339154075
Skewness Tinggi Badan  : -0.006355937698947297
Skewness  Berat Badan  : -0.05979606826320327
Skewness Ukuran Sepatu : -0.011844106877725483
```
