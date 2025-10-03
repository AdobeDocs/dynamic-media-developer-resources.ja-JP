---
title: contentUrl
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# contentUrl{#contenturl}

すべてのビューアに共通のパラメーター。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>カスタム CSS ファイル、クローズドキャプションコンテンツ、ナビゲーションコンテンツへのベースパスを指定します。 </p> <p>パスの先頭に/<span class="filepath"> という </span> がない場合は、ビューアのHTML ページの場所に対する相対パスになります。 パスの先頭 <span class="filepath">/</span> の場合は、同じサーバー上の絶対パスを指定します。 </p> <p> スタイルコマンドを指定しない場合、デフォルトの CSS ファイルの読み込みには影響しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

<!--

```
contentUrl=https://demos-pub.assetsadobe.com/
```

-->
