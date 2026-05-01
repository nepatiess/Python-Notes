# 🐍 Python Notes

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)

> Temel Python programlama kavramlarını kapsayan, egzersizlerle desteklenmiş kapsamlı ders notları.  
> A comprehensive Python notebook covering fundamentals with hands-on exercises.

---

## 📊 İstatistikler · Stats

| | |
|---|---|
| 📚 Bölüm / Sections | 7 |
| 🎮 Egzersiz / Exercises | 5 |
| 💻 Satır Kod / Lines of Code | 400+ |
| 🐍 Dil / Language | Python 3 |

---

## 📋 İçindekiler · Table of Contents

| # | Bölüm (TR) | Section (EN) |
|---|---|---|
| 01 | 🚀 Giriş | Introduction |
| 02 | ⚙️ Python Sözdizimi | Python Syntax |
| 03 | 🔀 Akış Kontrolü | Flow Controls |
| 04 | 🔧 Fonksiyonlar | Functions |
| 05 | 📦 Veri Yapıları | Data Structures |
| 06 | 📁 Dosya İşlemleri & Hatalar | Files & Errors |
| 07 | 🎮 Pratik Egzersizler | Practical Exercises |

---

## 01 · 🚀 Giriş · Introduction

**🇹🇷 Türkçe**  
Değişken tanımlama, veri tipleri (`int`, `float`, `str`), `input()` ile kullanıcıdan veri alma ve `datetime`, `random`, `math` gibi temel kütüphanelerin kullanımı.

**🇬🇧 English**  
Variable declaration, data types (`int`, `float`, `str`), collecting user input with `input()`, and using standard libraries like `datetime`, `random`, and `math`.

**Kavramlar · Concepts:** `int` `float` `str` `input()` `datetime` `random` `math` `type()`

```python
# yaş hesaplama / age calculation
import datetime
today = datetime.date.today()
age = today.year - 2003
print(f"Age: {age}")
```

---

## 02 · ⚙️ Python Sözdizimi · Python Syntax

**🇹🇷 Türkçe**  
Aritmetik operatörler (`+` `-` `*` `/` `%` `**` `//`), atama operatörleri (`+=` vb.), karşılaştırma ve mantıksal operatörler (`and`, `or`, `not`).

**🇬🇧 English**  
Arithmetic operators, assignment shorthands like `+=`, comparison operators, and logical operators (`and`, `or`, `not`) with Boolean logic tables.

**Kavramlar · Concepts:** `+ - * / % ** //` `+= -= *= /=` `and · or · not` `== != > < >= <=`

### Mantıksal Operatörler · Boolean Logic Table

| A | B | A and B | A or B | not A |
|---|---|---------|--------|-------|
| True | True | True | True | False |
| True | False | False | True | False |
| False | True | False | True | True |
| False | False | False | False | True |

```python
print("5+2=",  5+2)   # 7
print("5**2=", 5**2)  # 25
print("5//2=", 5//2)  # 2  (tam bölme / floor division)
print("5%2=",  5%2)   # 1  (kalan / remainder)
```

---

## 03 · 🔀 Akış Kontrolü · Flow Controls

**🇹🇷 Türkçe**  
`if/elif/else` koşulları, `for` ve `while` döngüleri, `break` ile döngü kırma, iç içe koşullar ve `range()` kullanımı.

**🇬🇧 English**  
`if/elif/else` conditionals, `for` and `while` loops, breaking loops with `break`, nested conditions, and iterating with `range()`.

**Kavramlar · Concepts:** `if / elif / else` `for` `while` `break` `range()` `continue`

### Akış Diyagramı · Flow Diagram

```
if koşul  →  True ise çalıştır  →  elif kontrol  →  else
while döngü  →  koşul True  →  işlem yap  →  break ile çık
```

```python
# sıcaklık kontrolü / temperature check
celcius = 32
if celcius > 30:
    print('Hot')
elif 30 >= celcius > 20:
    print('Good')
elif -273 < celcius <= 20:
    print('Cold')
else:
    print('Something went wrong!')
```

```python
# for döngüsü / for loop
for i in range(1, 101):
    if i % 5 == 0:
        print(i)
```

---

## 04 · 🔧 Fonksiyonlar · Functions

**🇹🇷 Türkçe**  
`def` ile fonksiyon tanımlama, varsayılan parametre değerleri, `return` ile değer döndürme, yerel/global değişken farkı (`global` anahtar kelimesi) ve modül import etme.

**🇬🇧 English**  
Defining functions with `def`, default parameter values, returning values with `return`, local vs global variable scope with the `global` keyword, and importing modules.

**Kavramlar · Concepts:** `def` `return` `global` `default params` `import` `seaborn` `matplotlib`

### Kapsam Farkı · Scope Difference

| | Yerel (Local) | Global |
|---|---|---|
| Tanımlandığı yer | Fonksiyon içinde | Fonksiyon dışında |
| Erişim | Sadece o fonksiyonda | Her yerden |
| Değiştirmek için | Normal atama | `global` keyword gerekli |

```python
# varsayılan parametre / default parameter
def greetings(first_name, last_name, auto_correction=True):
    if auto_correction:
        print("Hello,", first_name.capitalize(), last_name.capitalize())
    else:
        print("Hello,", first_name, last_name)

greetings('zEyNEp', 'kOz')  # → Hello, Zeynep Koz
```

```python
# global değişken / global variable
number = 13
def change_number():
    global number
    number = 4

change_number()
print(number)  # → 4
```

---

## 05 · 📦 Veri Yapıları · Data Structures

**🇹🇷 Türkçe**  
Liste metodları (`append`, `insert`, `remove`), dilimleme (slicing), sözlük (`dict`) oluşturma ve erişim, `items()`/`keys()`/`values()`, list comprehension ve unpacking.

**🇬🇧 English**  
List methods (`append`, `insert`, `remove`), slicing, creating and accessing dictionaries, iterating with `items()`/`keys()`/`values()`, list comprehension, and tuple unpacking.

**Kavramlar · Concepts:** `list[ ]` `dict{ }` `append` `insert` `remove` `slicing [a:b]` `list comprehension` `unpacking`

### Liste Metodları · List Methods

| Metod | Açıklama | Örnek |
|---|---|---|
| `append(x)` | Sona ekle / Add to end | `lst.append("Water")` |
| `insert(i, x)` | İndekse ekle / Insert at index | `lst.insert(2, "Banana")` |
| `remove(x)` | Değere göre sil / Remove by value | `lst.remove("Apple")` |
| `lst[i] = x` | İndeksi güncelle / Update index | `lst[3] = "Strawberry"` |

```python
# list comprehension örneği
number_list = [1, 2, 3, 4, 5]
square_list = [num ** 2 for num in number_list]
# → [1, 4, 9, 16, 25]

# sözlük döngüsü / dictionary loop
for key, value in inventory.items():
    if value > 200:
        print('Too many', key)
    else:
        print('Enough', key)
```

---

## 06 · 📁 Dosya İşlemleri & Hatalar · Files & Errors

**🇹🇷 Türkçe**  
Dosya açma (`open`), okuma/yazma modları (`'r'`, `'w'`), `with` bloğu kullanımı, `try/except` ile hata yakalama ve `ValueError`, `ZeroDivisionError` gibi özel hata türleri.

**🇬🇧 English**  
Opening files with `open()`, read/write modes (`'r'`, `'w'`), the `with` context manager, catching exceptions with `try/except`, and handling specific errors like `ValueError` and `ZeroDivisionError`.

**Kavramlar · Concepts:** `try / except` `open()` `read()` `write()` `with ... as` `ValueError` `ZeroDivisionError`

### Dosya Modları · File Modes

| Mod | Açıklama |
|---|---|
| `'r'` | Okuma / Read |
| `'w'` | Yazma (üzerine yazar) / Write (overwrites) |
| `'a'` | Ekleme / Append |

```python
# with bloğu / with block (önerilen yöntem / recommended)
with open('number_history.txt', 'w') as number_file:
    number_file.write("Hello World\n")

# hata yönetimi / error handling
def divide(number1, number2):
    try:
        return int(number1) / int(number2)
    except ValueError:
        return 'Only integers are allowed!'
    except ZeroDivisionError:
        return 'You cannot divide any number by zero!'
```

---

## 07 · 🎮 Pratik Egzersizler · Practical Exercises

| # | Başlık | Açıklama | Konular |
|---|---|---|---|
| 01 | Adventure Planning | Arkadaşla macera planlama | Değişkenler, listeler, random |
| 02 | Rock Paper Scissors 🪨📄✂️ | Taş-kağıt-makas oyunu | Döngüler, koşullar, random |
| 03 | Julia's NY Trip ✈️ | Yolculuk yardımcısı + birim dönüşümü | Fonksiyonlar, assert, matplotlib |
| 04 | My Supermarket 🛒 | Alışveriş listesi yönetimi | Liste metodları |
| 05 | Teacher Assistant 📝 | Not sistemi ve karne oluşturma | Dosyalar, hata yönetimi, döngüler |

---

## 📦 Bağımlılıklar · Dependencies

```bash
pip install seaborn matplotlib
```

| Kütüphane | Kullanım |
|---|---|
| `seaborn` | Veri görselleştirme / Data visualization |
| `matplotlib` | Grafik çizimi / Plotting |
| `random` | Rastgele sayı üretme / Random number generation |
| `datetime` | Tarih işlemleri / Date operations |
| `math` | Matematiksel işlemler / Math operations |
| `os`, `time` | Sistem işlemleri / System operations |

---

## 🚀 Nasıl Kullanılır? · How to Use?

**🇹🇷** Google Colab üzerinde açıp her hücreyi sırayla çalıştırın. Egzersizler her bölümün sonunda yer almaktadır.

**🇬🇧** Open in Google Colab and run each cell in order. Exercises appear at the end of each section.

---

*Python Notes · Zeynep Koz · Google Colab Notebook*
