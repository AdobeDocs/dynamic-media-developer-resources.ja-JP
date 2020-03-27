---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: CallToAction.fmt
solution: Experience Manager
title: CallToAction.fmt
topic: Dynamic media
uuid: c85160e2-431f-42af-a468-c754bfe86ecd
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.fmt{#calltoaction-fmt}

インタラクティブビデオビューアの設定属性。

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。 </p> <p>指定した形式が「<span class="codeph"> -alpha</span>」で終わる場合、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として扱われます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```

