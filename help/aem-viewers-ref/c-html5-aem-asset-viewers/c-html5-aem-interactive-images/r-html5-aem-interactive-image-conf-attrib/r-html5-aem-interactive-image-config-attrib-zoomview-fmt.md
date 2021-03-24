---
description: コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブ画像
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 末尾が<span class="codeph"> -alpha</span>の形式を指定すると、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として扱われます。 コンポーネントの背景はデフォルトで白になります。 したがって、透明にするには、<span class="codeph"> background-color</span> CSSプロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
