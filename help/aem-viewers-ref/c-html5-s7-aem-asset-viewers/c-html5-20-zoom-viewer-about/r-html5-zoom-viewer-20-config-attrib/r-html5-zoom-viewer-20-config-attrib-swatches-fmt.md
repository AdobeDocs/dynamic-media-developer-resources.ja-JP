---
description: 'null'
seo-description: 'null'
seo-title: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。 指定した形式が —alphaで終わる場合 <span class="codeph"></span>、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として処理されます。 デフォルトでは、コンポーネントの背景は白です。 したがって、背景を透明にするには、 <span class="codeph"> CSSプロパティbackground-color</span> をtransparentに設定 <span class="codeph"> します</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
