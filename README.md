# python-learning
作業療法士からAIアプリケーションエンジニア転職を目指して独学中。
Python基礎の学習記録リポジトリです。

---

## 学習環境

| ツール | 用途 |
|---|---|
| Google Colab | 1行ずつ実行して結果を確認しながら学習 |
| VS Code | 完成コードの保存・管理 |
| GitHub | 学習証跡の蓄積・公開 |

---

## 進捗

| 日付 | 内容 | ファイル |
|---|---|---|
| 2026-05-12 | Google ColabからVS Codeへの移行・GitHub使用方法習得 | - |
| 2026-05-12 | Python基礎（変数・データ型・文字列・型変換） | chapter01_03.py |
| 2026-05-13 | リスト・辞書・関数（def・return） | chapter04.py |
| 2026-05-14 | 外部ライブラリ・QRコード生成（qrcode） | chapter05.py |
| 2026-05-14 | 条件分岐・繰り返し（if文、比較演算子、elif、else、for文） | chapter06.py |
| 2026-05-15・16 | PDF操作自動化（PyMuPDF）、画像処理自動化（Pillow） | chapter07.py |
| 2026-05-18 | Webスクレイピング（requests・BeautifulSoup） | chapter08.py |
| 2026-05-19 | 機械学習（scikit-learn・NumPy・手書き数字認識） | chapter09.py |

---

## 日程ごとの学習内容（やさしい解説）

プログラミングに触れたことがない方でも分かるように、日付ごとに「何を学んだか」「何ができるようになったか」を整理しています。

### 2026-05-12｜開発環境の整備とPython基礎

**何をしたか**
- これまでブラウザ上で動く Google Colab を使っていましたが、本格的にコードを書くため **VS Code**（パソコンにインストールするコードエディタ）へ移行しました。
- 書いたコードをインターネット上に保存・公開できる **GitHub** の使い方を覚えました（SSHキー登録・コミット・プッシュ）。
- Pythonの基礎文法を学習しました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| `print()` | 画面に文字や数値を表示する命令 |
| 変数 | データに名前をつけて保管する「箱」（例：`a = 100`） |
| データ型 | データの種類のこと。整数(`int`)・小数(`float`)・文字列(`str`)・真偽値(`bool`) |
| 四則演算 | `+ - * /` に加え、切り捨て除算 `//`、余り `%` も使える |
| 文字列スライス | 文字列の一部を切り出す機能（例：`"Python仙人"[2:8]`） |
| f文字列 | 変数の中身を文字列に埋め込む書き方（例：`f"Hello,{name}"`） |
| 型変換 | 数値を文字列にしたり、文字列を数値に変えたりする操作 |

**できるようになったこと**: BMI計算など簡単な計算プログラムが書ける。

---

### 2026-05-13｜複数データの扱い・関数

**何をしたか**
- 複数のデータをまとめて扱う方法（リスト・辞書）と、処理に名前をつけて再利用する方法（関数）を学びました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| リスト | データを「順番に」並べて保管する箱（例：`["プリン", "ケーキ", "チョコ"]`） |
| 辞書 | 「キー」と「値」のペアで保管する箱（例：`{"下呂温泉": "岐阜県"}`） |
| `append()` / `extend()` | リストにデータを追加する命令 |
| `del` | リスト・辞書からデータを削除する命令 |
| `len()` | データの個数を数える命令 |
| 関数（`def`） | よく使う処理に名前をつけて、いつでも呼び出せるようにする仕組み |
| `return` | 関数から計算結果を返す命令（`print` は表示するだけ、`return` は別の場所で再利用できる値を返す） |

**できるようになったこと**: お菓子リスト・温泉地辞書のような「データのまとまり」を操作できる。三角形の面積を求める関数のように、自作の処理を作って何度でも呼び出せる。

---

### 2026-05-14｜外部ライブラリ・条件分岐・繰り返し

**何をしたか**
- Python本体にはない便利な機能を、追加インストールして使う方法を学びました（**外部ライブラリ**）。
- 条件によって処理を変える `if` 文、同じ処理を繰り返す `for` 文を学びました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| `pip install` | 外部ライブラリをインストールするコマンド |
| `import` | インストールしたライブラリを使えるように読み込む命令 |
| `random` | ランダムな数値を生成するライブラリ（例：おみくじアプリ） |
| `qrcode` | QRコード画像を生成するライブラリ |
| `if / elif / else` | 「もし○○なら〜」と条件で処理を分岐させる構文 |
| 比較演算子 | `==`（等しい）`!=`（等しくない）`<` `>` などの判定記号 |
| `for` 文 | 同じ処理を繰り返す構文 |
| `range()` | 連続する数値を作る関数（例：`range(1,10,2)` → 1,3,5,7,9） |
| ネストループ | `for` の中に `for` を入れて多重の繰り返しをする書き方（例：九九の表） |

**できるようになったこと**: QRコード生成・おみくじアプリ・九九の表など、小さなアプリが作れる。

---

### 2026-05-15・16｜ファイル操作の自動化（PDF・画像）

**何をしたか**
- 普段GUIで行う作業（PDFの結合・回転、画像のリサイズなど）を、Pythonで自動化する方法を学びました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| `PyMuPDF`（`pymupdf`） | PDFを操作するライブラリ |
| `get_text()` | PDFからテキストを抜き出す |
| `select()` | 指定ページだけを抽出 |
| `set_rotation()` | ページを回転 |
| `insert_file()` | 別のPDFを結合 |
| `delete_page()` | ページを削除 |
| `Pillow`（`PIL`） | 画像を操作するライブラリ |
| `Image.open()` | 画像ファイルを読み込む |
| `resize()` | 画像のサイズを変更 |
| `rotate()` | 画像を回転 |
| `convert("L")` | 画像をグレースケール（白黒）に変換（L = Luminance＝輝度） |

**できるようになったこと**: 大量のPDF・画像を一括処理する作業をプログラムで自動化できる。

---

### 2026-05-18｜Webスクレイピング

**何をしたか**
- Webページの情報をプログラムで取得し、必要な部分だけ抽出する技術（**Webスクレイピング**）を学びました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| `requests` | Webページの中身（HTML）を取得するライブラリ |
| `requests.get(url)` | 指定URLにアクセスしてレスポンスを取得 |
| `response.encoding` | 文字コードを指定（日本語サイトで文字化けを防ぐため `"utf-8"` を設定） |
| `BeautifulSoup` | HTMLを解析（パース）して必要な部分を取り出すライブラリ |
| `soup.find("h1")` | HTMLの中から最初の `<h1>` タグを探す |
| `.text` | タグの中の文字だけを取り出す |

**できるようになったこと**: ニュースサイトやブログから「見出しだけ」「本文だけ」を自動で抜き出すプログラムが書ける。

---

### 2026-05-19｜機械学習（手書き数字認識）

**何をしたか**
- AI開発の入口となる **機械学習** を初めて体験し、手書き数字を認識するモデルを作りました。

**学んだ用語**
| 用語 | やさしい説明 |
|---|---|
| 機械学習 | コンピュータがデータからパターンを学び、新しいデータを予測・判断する技術 |
| 教師あり学習 | 「問題」と「正解」のセットを大量に見せて学習させる方法（例：手書き数字の画像とその答え） |
| `scikit-learn` | Pythonで機械学習を行うための代表的ライブラリ |
| `datasets.load_digits()` | 8×8ピクセルの手書き数字画像が大量に入った練習用データセット |
| `digits.data` | 画像を「64個の数値の並び」に変換したもの |
| `digits.target` | 各画像の正解ラベル（0〜9） |
| `digits.images` | 元の8×8の画像データ |
| `matplotlib.pyplot`（`plt`） | グラフや画像を表示するライブラリ |
| `plt.imshow()` | 画像を表示する命令（`cmap="gray"` でグレースケール表示） |
| `SVC`（Support Vector Classifier） | 分類問題を解く機械学習アルゴリズムの一つ |
| `model.fit(データ, 正解)` | モデルにデータを学習させる |
| `model.predict([データ])` | 学習済みモデルで新しいデータの答えを予測する |
| `NumPy`（`np`） | 数値の配列を効率的に扱うライブラリ |
| `np.asarray()` | 画像データを数値の配列に変換 |
| `flatten()` | 二次元配列（8×8）を一次元（1×64）に並び替える |
| 白黒反転（`16 - digits.images`） | 学習データは「黒背景に白文字」前提のため、画像データを反転させて合わせる |
| 正規化（`* 17 // 256`） | 0〜255の輝度値を、学習データと同じ0〜16の範囲に変換する |

**機械学習の処理の流れ**

```
【学習フェーズ】
  画像データ(8×8) → 白黒反転 → 1×64に変換 → 正解ラベルと組にして学習(model.fit)
                                                      ↓
                                                 学習済みモデル
【予測フェーズ】
  新しい画像(0.jpg) → グレースケール化 → 8×8にリサイズ
                  → 0〜16に正規化 → 1×64にflatten → model.predict() → 予測結果
```

**できるようになったこと**: scikit-learnを使い、手書き数字を認識するAIモデルを作って自分の用意した画像（`0.jpg`）の数字を予測できる。

---

## 学習内容サマリー（章別）

### chapter01_03.py（第1〜3章）
- `print()` による出力
- 変数（文字列・数値・真偽値）
- 四則演算・BMI計算
- データ型（int・float・str・bool）と `type()` 関数
- 文字列操作（結合・スライス・`len()`）
- f文字列（`f"Hello,{name}"`）
- 型変換（`str()` / `int()` / `float()`）

### chapter04.py（第4章）
- リスト（作成・取得・更新・追加・削除・件数）
- 辞書（作成・取得・追加・更新・削除・結合）
- 関数（`def`・`print` と `return` の違い）

### chapter05.py（第5章）
- `random` モジュール（`random.randint()` で乱数生成）
- 外部ライブラリのインストール（`pip install`）
- `qrcode` ライブラリを使ったQRコード生成・保存

### chapter06.py（第6章）
- 条件分岐（`if` / `elif` / `else`）
- `random.randint()` を使ったおみくじアプリ
- `for` ループによるリストの反復処理
- `range()` 関数（開始・終了・ステップ指定）
- ネストされた `for` ループ（九九の計算表）

### chapter07.py（第7章）
- `PyMuPDF` によるPDF操作自動化
  - テキスト抽出（`get_text()`）
  - ページ抽出・保存（`select()`）
  - ページ回転（`set_rotation()`）
  - PDFの結合（`insert_file()`）
  - ページ削除（`delete_page()`）
- `Pillow` による画像処理自動化
  - 画像サイズ取得（`img.size`）
  - リサイズ（`resize()`）
  - 回転（`rotate()`）
  - グレースケール変換（`convert("L")`）

### chapter08.py（第8章）
- `requests` によるWebページの取得（`requests.get()`）
- レスポンスのエンコーディング指定（`response.encoding`）
- `BeautifulSoup` によるHTMLパース（`html.parser`）
- タグ単位でのデータ抽出（`soup.find()`・`.text`）

### chapter09.py（第9章）
- `scikit-learn` による教師あり学習の体験
  - `datasets.load_digits()`：手書き数字データセットの読み込み
  - データの形状確認（`digits.data.shape` / `digits.target` / `digits.images`）
  - `matplotlib.pyplot` による画像表示（`plt.imshow()`）
  - 白黒反転処理（`16 - digits.images`）
  - `sklearn.svm.SVC` による分類モデルの作成
  - `model.fit()` で学習、`model.predict()` で予測
- `NumPy` を用いた画像データの前処理
  - `np.asarray()` で画像を数値配列に変換
  - 0〜16の範囲への正規化（`* 17 // 256`）
  - `flatten()` による2次元→1次元変換
- `Pillow` との連携：自作画像の読み込み・グレースケール化・8×8リサイズ

---

## 学習した主な構文

### 第1〜3章：Python基礎

```python
# 出力・変数
print("Hello Python")
a = 100
b = "Hello Python"

# 四則演算
print(1 + 2)   # 足し算
print(2 - 1)   # 引き算
print(1 * 2)   # 掛け算
print(1 / 2)   # 割り算
print(3 // 2)  # 切り捨て除算
print(5 % 2)   # 余り

# BMI計算
height = 1.75
weight = 70
bmi = weight / (height * height)
print(bmi)

# データ型と type()
i = 123
f = 1.23
s = "ぱいせん"
b = True
print(type(i), type(f), type(s), type(b))

# 文字列操作
my_name = "私はPython仙人"
print(len(my_name))     # 文字数
print(my_name[2])       # インデックス指定
print(my_name[-2])      # 後ろからインデックス
print(my_name[2:8])     # スライス
print(my_name[1:8:2])   # ステップ付きスライス

# f文字列
name = "ぱいせん"
message = f"Hello,{name}"
print(message)

# 型変換
str_num = str(12.3)          # 数値 → 文字列
int_num = int("123")         # 文字列 → 整数
float_num = float("123.45")  # 文字列 → 小数
print("富士山の高さは" + str(3776) + "メートルです")
```

### 第4章：リスト・辞書・関数

```python
# リスト
sweets = ["プリン", "ケーキ", "チョコ"]
print(sweets[0])          # 取得
sweets[1] = "アイス"      # 更新
sweets.append("アイス")   # 追加（1件）
sweets.extend(["アイス", "クッキー"])  # 追加（複数）
del sweets[1]             # 削除
print(len(sweets))        # 件数

# 辞書
onsen = {"下呂温泉": "岐阜県", "草津温泉": "群馬県"}
print(onsen.get("下呂温泉"))        # 取得
onsen["有馬温泉"] = "兵庫県"        # 追加
onsen["下呂温泉"] = "岐阜県下呂市"  # 更新
rivers1.update(rivers2)            # 結合
del rivers1["天塩川"]              # 削除

# 関数
def add_numbers(a, b):
    return a + b

output = add_numbers(5, 7)
print(output)  # → 12

def triangle_area(base, height):
    area = base * height / 2
    return area
```

### 第5章：外部ライブラリ

```python
# 乱数
import random
num = random.randint(1, 10)  # 1〜10のランダムな整数
print(num)

# QRコード生成
import qrcode
img = qrcode.make("Python楽しい!")
img.save("qrcode.png")
```

### 第6章：条件分岐・繰り返し

```python
# if / elif / else
weather = "雨"
if weather == "晴れ":
    print("お買い物へ行きます")
elif weather == "雨":
    print("お家でゴロゴロします")
else:
    print("近所をお散歩します")

# おみくじ（randint + if）
omikuji = random.randint(0, 3)
if omikuji == 0:
    print("大吉")
elif omikuji == 1:
    print("中吉")
else:
    print("小吉")

# for ループ
names = ["oda", "toyotomi", "tokugawa"]
for name in names:
    print(name)

for i in range(5):        # 0〜4
    print(i)

for i in range(1, 10, 2): # 1,3,5,7,9（ステップ2）
    print(i)

# ネストされたforループ（九九）
for i in range(1, 10):
    for j in range(1, 10):
        print(f"{i}×{j}={i*j}")
```

### 第7章：PDF操作・画像処理

```python
# PDF操作（PyMuPDF）
import pymupdf

doc = pymupdf.open("error.pdf")
text = doc[0].get_text()   # テキスト抽出
doc.close()

doc.select([0])            # 1ページ目のみ抽出
doc.save("error_1page.pdf")

doc[0].set_rotation(90)    # ページ回転
doc.save("rotated.pdf")

doc_a.insert_file(doc_b)   # PDF結合
doc_a.save("inserted.pdf")

doc.delete_page(2)         # ページ削除
doc.save("deleted.pdf")

# 画像処理（Pillow）
from PIL import Image

img = Image.open("sample.jpg")
print(f"画像の幅は{img.size[0]}")  # サイズ取得
print(f"画像の高さは{img.size[1]}")

resized_img = img.resize((int(img.size[0]*2), int(img.size[1]*0.5)))
resized_img.save("resized.jpg")     # リサイズ

rotated_img = img.rotate(90)
rotated_img.save("rotated.jpg")     # 回転

grayscale_img = img.convert("L")
grayscale_img.save("grayscale.jpg") # グレースケール変換
```

### 第8章：Webスクレイピング

```python
# Webページ取得（requests）
import requests

url = "https://miyashinblog.com/books/sample.html"
response = requests.get(url)
response.encoding = "utf-8"  # 文字化け防止
print(response.text)         # HTMLソース表示

# HTMLパース（BeautifulSoup）
from bs4 import BeautifulSoup

soup = BeautifulSoup(response.text, "html.parser")
print(soup.find("h1").text)  # h1タグのテキスト取得
print(soup.find("h2").text)  # h2タグのテキスト取得
print(soup.find("p").text)   # pタグのテキスト取得
```

### 第9章：機械学習（手書き数字認識）

```python
# データセットの読み込み
from sklearn import datasets
digits = datasets.load_digits()

print(digits.data.shape)   # (1797, 64)：1797枚×64画素
print(digits.target[:5])   # 先頭5枚の正解ラベル
print(digits.images[0])    # 1枚目の8×8画像データ

# 画像表示
import matplotlib.pyplot as plt
plt.imshow(digits.images[0], cmap="gray")
plt.show()

# 白黒反転（学習データに合わせる）
inverted_imgs = 16 - digits.images
plt.imshow(inverted_imgs[0], cmap="gray")
plt.show()

# モデルの学習
import sklearn.svm
model = sklearn.svm.SVC()
model.fit(16 - digits.data, digits.target)  # 反転データで学習

# 新しい画像で予測（前処理）
from PIL import Image
import numpy as np

image = Image.open("0.jpg")
grayscale_img = image.convert("L")          # グレースケール化
resize_img = grayscale_img.resize((8, 8))   # 8×8にリサイズ

num_img = np.asarray(resize_img, dtype=int) # 数値配列に変換
normalized_img = num_img * 17 // 256        # 0〜16に正規化
flattened_img = normalized_img.flatten()    # 1×64に変換

# 予測
pred = model.predict([flattened_img])
print(pred)  # → [0]（予測結果）
```

---

## GitHub学習記録（2026-05-12）

初めてGitHubを使用し、以下を習得：
- SSHキーの生成・GitHubへの登録
- リポジトリの作成・クローン
- 毎日のコミット手順（add → commit → push）
- .gitignoreの設定（.DS_Storeの除外）
- コミットメッセージの書き方

---

## フォルダ構成

```
python-learning/
├── README.md
├── .gitignore
├── 01_basics/
│   ├── chapter01_03.py   # 第1〜3章
│   ├── chapter04.py      # 第4章
│   ├── chapter05.py      # 第5章
│   ├── chapter06.py      # 第6章
│   ├── chapter07.py      # 第7章
│   ├── chapter08.py      # 第8章
│   └── chapter09.py      # 第9章
└── notes/
    ├── 2026-05-12.md     # 環境構築・Python基礎
    ├── 2026-05-13.md     # リスト・辞書・関数
    ├── 2026-05-14.md     # 外部ライブラリ・条件分岐・繰り返し
    ├── 2026-05-15_16.md  # PDF操作・画像処理
    ├── 2026-05-18.md     # Webスクレイピング
    ├── 2026-05-19.md     # 機械学習
    └── 2026-05-20.md
```

---

## 使用教材
- 作りたいものがない人のためのPython入門（KS情報科学専門書）
