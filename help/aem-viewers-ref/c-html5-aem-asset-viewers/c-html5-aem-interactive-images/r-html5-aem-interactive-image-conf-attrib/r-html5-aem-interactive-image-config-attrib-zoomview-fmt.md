---
title: ZoomView.fmt
description: コンポーネントが Image Server からの画像の読み込みに使用する画像形式を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a023abb-71c7-4db5-8d05-bf0a4b1fc3a0
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# ZoomView.fmt{#zoomview-fmt}

コンポーネントが Image Server からの画像の読み込みに使用する画像形式を指定します。

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 末尾が <span class="codeph"> -alpha</span> の形式を指定すると、画像が透明のコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、コンポーネントは画像を不透明として扱います。 コンポーネントの背景はデフォルトで白です。 したがって、透明にするには、CSS プロパティ <span class="codeph"> background-color</span> を <span class="codeph"> transparent</span> に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
