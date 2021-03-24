---
description: すべてのビューアに共通のパラメータ。
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Mediaクラシック，ビューア，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---


# videoServerUrl{#videoserverurl}

すべてのビューアに共通のパラメータ。

>[!NOTE]
>
>このコマンドはビデオ画像ビューアには適用されません。

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオサーバのルートパス。 ドメインが指定されていない場合は、ページの供給元のドメインが適用されます。 標準のURIパス解決が適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）標準のソフトウェアサービスの使用には必要ありません。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```

