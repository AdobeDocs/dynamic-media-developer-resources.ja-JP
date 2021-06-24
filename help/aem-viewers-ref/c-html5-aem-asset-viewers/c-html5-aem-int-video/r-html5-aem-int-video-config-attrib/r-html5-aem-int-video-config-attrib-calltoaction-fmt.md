---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# CallToAction.fmt{#calltoaction-fmt}

インタラクティブビデオビューアの設定属性。

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverから画像を読み込む際に使用する画像形式を指定します。 </p> <p>指定した形式が「<span class="codeph"> -alpha</span>」で終わる場合、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 </p> </td> 
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
