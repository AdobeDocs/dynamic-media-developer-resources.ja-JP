---
description: コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。
seo-description: コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: 73a2196f-0ece-497a-9a12-376dafbbae56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.fmt{#zoomview-fmt}

コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定した形式が —alphaで終わる場合 <span class="codeph"></span>、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として処理されます。 コンポーネントの背景色はデフォルトで白です。 したがって、透明にするには、 <span class="codeph"> CSSプロパティbackground-color</span> をtransparentに設定 <span class="codeph"> します</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
