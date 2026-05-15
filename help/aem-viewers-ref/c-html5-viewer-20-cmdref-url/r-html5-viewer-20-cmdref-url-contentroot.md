---
title: contentUrl
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
TQID: 'https://experienceleague.adobe.com/D95dvILCIpQtQ6D1TcPwj-xfgjXb6AvyMmm5vDlemWw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

---

# contentUrl{#contenturl}

すべてのビューアに共通のパラメーター。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>カスタム CSS ファイル、クローズドキャプションコンテンツ、またはナビゲーションコンテンツへのベースパスを指定します。 </p> <p>パスに先頭の<span class="filepath"> /</span>がない場合は、ビューアのHTML ページの場所を基準としています。 パスの先頭に<span class="filepath"> /</span>がある場合は、同じサーバー上の絶対パスを指定します。 </p> <p> スタイルコマンドを指定しない場合、デフォルトのCSS ファイルの読み込みに影響しません。 </p> </td> 
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
