**Diagnosis**

0 -- 3139

1 -- 1993

1993 tane diabet teşhisi olduğunu söyleyen bir datamız var.

**Gender**

M 3256

F 1875

f 1

Cinsiyet olarak 3 sınıf var görünüyordu 'f' olan değer 'F' olarak değişitirildi ve sonuç;

M 3256

F 1876

Böylece 3256 adet erkek, 1876 adet kadın olduğunu söylemek mümkün

**info**

0 Unnamed: 0 5132 non-null int64

1 Age 5132 non-null int64

2 Gender 5132 non-null object

3 BMI 5132 non-null int64

4 Chol 5132 non-null float64

5 TG 5132 non-null float64

6 HDL 5132 non-null float64

7 LDL 5132 non-null float64

8 Cr 5132 non-null float64

9 BUN 5132 non-null float64

10 Diagnosis 5132 non-null int64

**gender verisi harici numeric değerler var. Hesaplamalar yapılırken gender verisi ya sayılmayacak ya da kadın erkek sayısal değerlere çevrilecek.**

---

**null().sum()**

Unnamed: 0 0

Age 0

Gender 0

BMI 0

Chol 0

TG 0

HDL 0

LDL 0

Cr 0

BUN 0

Diagnosis 0

----Hiç boş veri yok---

**df["Age"].nunique()**

71 farklı yaş içeren bir veri seti

**SINIFLARIN DAĞILIMI**

veri sayısı: 5132

sınıf sayısı: 2

sınıfların dağılımı: Diagnosis

0 3139

1 1993

Name: count, dtype: int64

sınıfların 100'de kaçlık dilimde olduğu: Diagnosis

0 0.611652

1 0.388348

**CİNSİYET(GENDER) OBJESİ NUMERİC OLMASI İÇİN DEĞİŞTİRİLDİ**

Male: 0

Female: 1 olarak değişitirldi.

**Klasik Makine Öğrenmesi ile**

LR accuracy: 0.8227848101265823

SVC accuracy: 0.9629990262901655

RF accuracy: 0.9990262901655307

DT accuracy: 1.0

KNN accuracy: 0.9425511197663097

çok hızlı çalıştı ve en başarılı sonucu Decision Tree(karar ağaçları) algoritması verdi.

**\*BAŞARISI**

optimizer='adam'

model.add(Dense(8, input_dim=input_layer, activation='relu'))

model.add(Dense(1, activation='sigmoid'))

parametreleri ile 0.95 başarı elde edildi.

model.add(Dense(128, input_dim=input_layer, activation='relu'))

model.add(Dense(64, activation='relu'))

model.add(Dense(16, activation='relu'))

model.add(Dense(1, activation='sigmoid'))

optimizer=rmsprop

parametreleri ile 0.96 başarı elde edildi.

modelimiz **başarılı** bir şekilde eğitildi.
