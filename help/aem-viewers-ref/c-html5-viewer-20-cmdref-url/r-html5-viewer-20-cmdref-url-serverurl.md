---
description: すべてのビューアに共通のパラメータ。
seo-description: すべてのビューアに共通のパラメータ。
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic Media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# serverUrl{#serverurl}

すべてのビューアに共通のパラメータ。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>画像サービングの相対的または絶対的なルートパス </p> <p> ビューアで画像を取得する画像サービングの相対パスまたは絶対パスを指定します。 パスの先頭に<span class="filepath"> /</span>がない場合、ビューアのHTMLページからの相対パスになります。 パスの先頭に<span class="filepath"> /</span>がある場合、同じサーバの絶対パスになります。 </p> <p> ビューアで電子メール共有モジュールが有効になっている場合に備えて、絶対パスのみを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）標準的なSaaS(Software As Service)の使用には必要ありません。

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

