---
title: serverUrl
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
TQID: 'https://experienceleague.adobe.com/SbAeHSjxnw-69wsu92UeoEeGLlk3Ykpechs65I-k5EY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# serverUrl{#serverurl}

すべてのビューアに共通のパラメーター。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>画像サービングルートパスの相対または絶対。 </p> <p> ビューアが画像を取得する場所から、画像サービングへの相対パスまたは絶対パスを指定します。 パスに先頭の<span class="filepath"> /</span>がない場合は、ビューアのHTML ページの場所を基準としています。 パスの先頭に<span class="filepath"> /</span>がある場合は、同じサーバー上の絶対パスを指定します。 </p> <p> 電子メール共有モジュールがビューアで有効になっている場合は、絶対パスのみを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。 標準的なSaaS （Software as a Service）の使用には必要ありません。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
