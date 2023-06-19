# HTMLの学習メモ

## 基本構造

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        header
    </head>
    <body>
        body
    </body>
</html>
```

で構成

headはページの設定とか情報（タイトルとか）を付加する場所？

bodyはページ自体の内容を記述する場所

## body

### h
ヘッダ、でかい文字

h1~6まである、数字がでかいほどサイズが小さくなる

### p
普通の文字

### a
リンクの挿入、文字にリンク情報を付加したり色々できる

```html
<a href="URL" >hoge</a>
```
hrefが飛ぶリンク

aが囲むのは他のタグでもいいのでpとかimg(画像)とか括れる

### img
画像を挿入できる
```html
<img src="src" alt="alt">
```
srcで画像を指定、ローカルパスかURLで指定

altで代替情報を付加、読み込まれない場合でも内容を測れる

### figure
画像に説明文とかをつける用？

### figcaption
figure内でimgと一緒に使って画像にキャプションをつける

```html
<figure>
    <img src=cat.jpg alt="cat">
    <figcaption>猫</figcaption>
</figure>
```

### section
セクション、区切り、そのまま

内容を一纏めにしたい場合に使う
```html
<section>
    <p>hogeeeeeeee</p>
    <p>hegeeeeeeee</p>
</section>
```

### ul
箇条書き、ulの中にliで連ねる

```html
<ul>
    <li>a</li>
    <li>b</li>
    <li>c</li>
</ul>
```

### ol
数字付き箇条書き、勝手にインクリメントされる

こっちも中でliで連ねる

```html
<ol>
    <li>a</li>
    <li>b</li>
    <li>c</li>
</ol>
```

### form
サーバーに情報を送る用の区間を表す

中にinputとかで入力可能な部分を作る

### input
情報を入力するためのタグ、typeで色々種類がある

ラジオボタンの場合、選択を一つに限定するためにname値を設定する

```html
<form>
    <input type="text" name="name" placeholder="textbox" require>
    <input type="radio" name="hoge" value="hoge1">
    <input type="radio" name="hoge" value="hoge2">
    <input type="checkbox" checked> hige
```
textでテキストボックス、placeholderは内部にある透かし文字

radioでラジオボタン、nameの指定が無いと複数個選べてしまうので同じnameを指定して同時選択不能にする

checkboxでチェックボックス、複数選択可な場合に使用

valueで選択した場合の入力値を指定する、指定しないとonが帰る？

requireで入力必須に、checkedでデフォルト選択済みにできる

### button
ボタン、こっちもtypeで種類があるっぽい
```html
<button type="submit">Submit</button>
```
中にテキストを入れられる

### fieldset
一纏めにしたいformの内容を括る用

### legend
fieldsetの説明を付ける

### label
単一で文字を保持できないタグ用？

タグを囲める
```html
<label>
    <input type="radio" name="hoge">
    hoge
</label>
```

### footer
mainと同列最下部に配置する要素を入れる

## head

### title
タブに表示されるタイトル

### meta
振る舞いを指定する、文字コードの指定とか
```html
<meta charset="UTF-8">
```