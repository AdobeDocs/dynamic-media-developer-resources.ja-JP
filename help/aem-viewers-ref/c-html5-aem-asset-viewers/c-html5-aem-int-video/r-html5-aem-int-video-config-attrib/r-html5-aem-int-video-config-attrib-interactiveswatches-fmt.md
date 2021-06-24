---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: InteractiveSwatches.fmt
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

インタラクティブビデオビューアの設定属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverから画像を読み込む際に使用する画像形式を指定します。 </p> <p>指定した形式が「<span class="codeph"> -alpha</span>」で終わる場合、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 コンポーネントの背景はデフォルトで白です。 したがって、完全に透明にするには、CSSプロパティ<span class="codeph"> background-color</span>を<span class="codeph"> transparent</span>に設定します。 </p> </td> 
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
