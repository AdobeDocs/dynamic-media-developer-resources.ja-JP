---
title: serverUrl
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---

# serverUrl{#serverurl}

すべてのビューアに共通のパラメーター。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>画像サービングのルートパスの相対パスまたは絶対パス。 </p> <p> ビューアが画像を取得する画像サービングへの相対パスまたは絶対パスを指定します。 パスの先頭に/</span> という <span class="filepath"> がない場合は、ビューアHTMLページの場所を基準とした相対パスになります。 パスの先頭 <span class="filepath">/</span> の場合は、同じサーバー上の絶対パスを指定します。 </p> <p> ビューアでメール共有モジュールが有効になっている場合は、絶対パスのみを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。 標準的な SaaS （software as a service）の使用には不要です。

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
