---
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic，ビューア，SDK/API
role: Developer,Business Practitioner
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# serverUrl{#serverurl}

すべてのビューアに共通のパラメーター。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>画像サービングの相対的または絶対的なルートパス </p> <p> ビューアが画像を取得する画像サービングの相対パスまたは絶対パスを指定します。 パスの先頭に<span class="filepath"> /</span>がない場合、ビューアのHTMLページからの相対パスになります。 パスの先頭に<span class="filepath"> /</span>がある場合は、同じサーバ上の絶対パスを指定します。 </p> <p> ビューアで電子メール共有モジュールが有効になっている場合には、絶対パスのみを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）標準のSaaS（サービスとしてのソフトウェア）の使用には不要です。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
