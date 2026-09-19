# マイアプリ テンプレート

よく使うWebサイトやSNS、動画、地図などを、スマホのアプリ画面のようにまとめられるHTMLテンプレートです。

このテンプレートには **OJapp Free** が導入済みです。GitHubのテンプレートをコピーして少し書き換えるだけで、自分専用のアプリを作れます。

プログラムを最初から書く必要はありません。

## 作り方

### 1. テンプレートを自分のGitHubへコピーする

このリポジトリ上部の **Use this template** を押します。

1. **Create a new repository** を選ぶ
2. Repository nameに好きな名前を入力する
3. 公開する場合は **Public** を選ぶ
4. **Create repository** を押す

これで、自分のGitHubアカウントにテンプレートがコピーされます。

### 2. `index.html`を書き換える

コピーしたリポジトリで`index.html`を開き、鉛筆マークの **Edit this file** を押します。

HTML内で `【編集` を検索すると、変更する場所が見つかります。

1. **アプリ名・説明・ホーム画面アイコン**
2. **全体の色と見た目**
3. **画面上部の文章**
4. **表示するアプリ一覧**

変更が終わったら **Commit changes** を押して保存します。

## アプリ一覧の書き換え方

アプリ一覧は、次の部分を書き換えます。

```js
{
  name: "ショップ",
  url: "https://example.com/shop/",
  icon: "🛍️",
  color: "#fff0f4"
}
```

- `name`：アイコンの下に表示する名前
- `url`：開きたいWebページやSNSなどのURL
- `icon`：絵文字または画像URL
- `color`：アイコンの背景色

`{ ... }`をコピーすれば、アプリを何個でも追加できます。

### ファビコンを自動で表示する

`icon`を空にすると、URLからファビコンを自動取得します。

```js
{
  name: "YouTube",
  url: "https://www.youtube.com/",
  icon: "",
  color: "#ffffff"
}
```

ファビコンを取得できなかった場合は、代わりの記号が表示されます。

## GitHub Pagesで公開する

編集したページをGitHub Pagesで公開します。

1. リポジトリの **Settings** を開く
2. 左側のメニューから **Pages** を選ぶ
3. **Source** で **Deploy from a branch** を選ぶ
4. Branchを **main**、フォルダを **/(root)** にする
5. **Save** を押す

しばらくすると、次のような公開URLが表示されます。

```text
https://ユーザー名.github.io/リポジトリ名/
```

## ホーム画面に追加する

完成したGitHub PagesのURLをスマホで開きます。

- **iPhone**：Safariの共有ボタン →「ホーム画面に追加」
- **Android**：Chromeのメニュー →「ホーム画面に追加」または「アプリをインストール」

ホーム画面に追加したアイコンから開くと、アプリのような画面で起動します。

ホーム画面から起動した場合、画面下の追加案内は自動で非表示になります。

## ホーム画面アイコンについて

`index.html`内にある次のURLを、自分の正方形画像へ変更してください。

```html
<meta name="ojapp:icon" content="https://example.com/icon.webp">
```

画像は **512×512pxの正方形画像** を推奨します。

画像をリポジトリへ追加した場合は、次のようにファイル名を指定できます。

```html
<meta name="ojapp:icon" content="./icon.webp">
```

## OJapp Free

このテンプレートは、次の1行でページをホーム画面アプリ化しています。

```html
<script src="https://ojapp.app/js/ojapp_1p1a.js"></script>
```

[OJapp Freeについて](https://ojapp.app/one-page-one-app)
