---
description: すべてのビューアに共通のパラメータ。
solution: Experience Manager
title: contentUrl
feature: Dynamic Mediaクラシック，ビューア，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# contentUrl{#contenturl}

すべてのビューアに共通のパラメータ。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>カスタムCSSファイル、クローズドキャプションコンテンツまたはナビゲーションコンテンツへの基本パスを指定します。 </p> <p>パスの先頭に<span class="filepath"> /</span>がない場合、ビューアのHTMLページからの相対パスになります。 パスの先頭に<span class="filepath"> /</span>がある場合、同じサーバの絶対パスになります。 </p> <p> スタイルコマンドを指定しない場合、初期設定のCSSファイルの読み込みに影響しません。 </p> </td> 
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

