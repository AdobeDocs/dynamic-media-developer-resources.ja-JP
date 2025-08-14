---
title: style
description: style
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 7%

---

# style{#style}

次のコマンドは、URL クエリ文字列および設定の両方から適用できます。 URL クエリ文字列に適用されるコマンドは、常に config に存在する同じコマンドよりも優先されます。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> CSS の相対位置または絶対位置。 </p> <p>カスタム CSS ファイルの場所を指定します。 <span class="codeph"><span class="varname"> cssPath</span></span> が相対パスの場合は、ビューアのHTML ページの場所と、contentUrl=<span class="codeph"> パラメーターの値 </span> 対して解決されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS ファイル内のすべてのアセット参照は、呼び出し元のHTML ページの場所ではなく、CSS ファイルの場所に対して解決されます。

## プロパティ {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

オプション。

## 初期設定 {#section-79a827f7a3bb4f36b3d72c309155059e}

なし

## 例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
