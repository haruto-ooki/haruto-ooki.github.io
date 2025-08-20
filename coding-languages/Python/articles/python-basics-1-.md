---
layout: default
title: Python Basics -1-
---

# Python入門 ① - 基本・変数・データ型

この講座では、Pythonの基本的な文法、変数の概念、主要なデータ型について学びます。初心者向けの内容です。

---

## 🐍 1. Pythonとは？

- 読みやすく、書きやすいプログラミング言語  
- Web開発、AI、データ分析などに使われる  
- 無料で使えるオープンソース  

---

## 🧘 2. 最初のコード

```python
print("Hello, Python")
```

- `print()` は画面に文字や数値を表示する関数
- 実行すると `Hello, Python` が出力される

---

## 🔢 3. 数値と演算

```python
print(2 + 3)    # 足し算

# 5

print(10 - 4)   # 引き算

# 6

print(5 * 6)    # 掛け算

# 30

print(8 / 2)    # 割り算（float型になる）

# 4.0

print(7 // 2)   # 商（整数）

# 3

print(7 % 2)    # 余り

# 1

print(2 ** 3)   # 累乗（2の3乗）

# 8

```

---

## 📦 4.変数の基本

### 変数とは？

- 値を一時的に保存する「名前付きの箱」
- `=` を使って代入する

```python
name = "Taro"
age = 20
print(name)
print(age)
```

### 命名ルール

- 英字、数字、アンダースコアが使える
- 数字で始めてはいけない
- Pythonの予約語は使えない（例：print, if）

### 代入と更新

```python
x = 10
y = x
x = x + 5
print(x)  # 15
print(y)  # 10
```

### 複数代入

```python
a, b, c = 1, 2, 3
print(a, b, c)
```

---

## 🧠 5. データ型の基礎

主な型一覧


| 型名   | 説明             | 例                     |
|--------|------------------|------------------------|
| int    | 整数             | `10`, `-3`             |
| float  | 小数             | `3.14`, `2.0`          |
| str    | 文字列           | `"Hello"`              |
| bool   | 真偽値           | `True`, `False`        |
| list   | 順序付きの配列   | `[1, 2, 3]`            |
| dict   | キーと値のペア   | `{"a": 1, "b": 2}`     |
| tuple  | 変更不可の配列   | `(1, 2)`               |
| set    | 重複なしの集合   | `{1, 2, 3}`            |

---

## 🔍 6. 各型の詳細

### int型（整数）

```python
x = 100
print(type(x))  # <class 'int'>
```

### float型（小数）

```python
y = 3.14
print(type(y))  # <class 'float'>
print(2 + 3.0)  # 5.0（float型になる）
```

型変換

```python
a = 10
b = float(a)    # 10.0

c = int(3.99)   # 3（小数点以下切り捨て）
```

誤差の例

```python
print(0.1 + 0.2)  # 0.30000000000000004
```

精密計算をしたい場合

```python
from decimal import Decimal
print(Decimal("0.1") + Decimal("0.2"))  # 0.3
```

---

### str型（文字列）

```python
text = "Hello"
print(text + " World")   # 結合
print(text * 3)          # 繰り返し
print(text[0])           # インデックス
```

---

### bool型（真偽値）

```python
is_ok = True
print(type(is_ok))  # <class 'bool'>
print(5 > 3)         # True
print(2 == 4)        # False
```

---

### list型（リスト）

```python
scores = [80, 90, 70]
print(scores[1])         # 90
scores.append(100)       # 追加
scores.remove(70)        # 削除
print(len(scores))       # 要素数
```

---

### dict型（辞書）

```python
user = {"name": "Taro", "age": 20}
print(user["name"])      # Taro
user["age"] = 21         # 更新
user["gender"] = "M"     # 追加
```

---

### tuple型（タプル）

```python
point = (10, 20)
print(point[0])          # 10
```

---

### set型（集合）

```python
nums = {1, 2, 3, 2}
print(nums)              # {1, 2, 3}

a = {1, 2, 3}
b = {3, 4, 5}
print(a | b)             # 和集合
print(a & b)             # 積集合
print(a - b)             # 差集合
```

---

## 🧪 7. 型の確認と変換

```python
print(type(100))         # <class 'int'>
print(type("abc"))       # <class 'str'>
print(type([1, 2, 3]))    # <class 'list'>

x = str(123)             # "123"
y = int("456")           # 456
z = float("7.89")        # 7.89
```

---

## 📝 8. コメントの書き方

```python
# これはコメントです
print("テスト")  # この行の右側にもコメントを書ける
```

---

## ⚠️ 9. エラーの例

```python
print("Hello"  # 括弧が閉じていない
```

出力：

```python
SyntaxError: unexpected EOF while parsing
```

---

## 🚀 10. 次に学ぶこと
- 条件分岐（if文）
- 繰り返し（for文、while文）
- 関数の定義
- クラスとオブジェクト
- ファイル操作
