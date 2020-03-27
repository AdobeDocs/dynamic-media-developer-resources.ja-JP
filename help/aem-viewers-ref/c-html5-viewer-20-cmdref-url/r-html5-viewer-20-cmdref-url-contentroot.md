---
description: すべてのビューアに共通のパラメータ。
seo-description: すべてのビューアに共通のパラメータ。
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# contentUrl{#contenturl}

すべてのビューアに共通のパラメータ。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span></span> </p> </td> 
   <td colname="col2"> <p>カスタムCSSファイル、クローズドキャプションコンテンツ、またはナビゲーションコンテンツのベースパスを指定します。 </p> <p>パスの先頭に/がない場 <span class="filepath"> 合は、</span>ビューアのHTMLページからの相対パスになります。 パスの先頭に/がある場 <span class="filepath"> 合は、</span>同じサーバの絶対パスを指定します。 </p> <p> スタイルコマンドを指定しない場合、初期設定のCSSファイルの読み込みに影響しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

