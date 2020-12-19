---
description: 'null'
seo-description: 'null'
seo-title: style
solution: Experience Manager
title: style
topic: Dynamic media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 8%

---


# style{#style}

次のコマンドは、URLクエリ文字列とconfigの両方から適用できます。 URLクエリ文字列で適用するコマンドは、configに存在する同じコマンドよりも常に優先されます。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相対的または絶対的なCSSの場所 </p> <p>カスタムCSSファイルの場所を指定します。 <span class="codeph"><span class="varname"> cssPath</span></span>が相対パスの場合、ビューアのHTMLページの位置と<span class="codeph"> contentUrl=</span>パラメータの値を基準に解決されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSSファイル内のすべてのアセット参照は、呼び出し元のHTMLページではなく、CSSファイルの場所を基準に解決されます。

## プロパティ {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

（オプション）

## 初期設定 {#section-79a827f7a3bb4f36b3d72c309155059e}

なし

## 例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
