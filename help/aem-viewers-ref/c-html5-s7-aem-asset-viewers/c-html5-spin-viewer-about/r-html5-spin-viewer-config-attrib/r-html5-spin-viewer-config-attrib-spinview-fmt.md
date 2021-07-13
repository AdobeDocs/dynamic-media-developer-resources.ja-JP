---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,User
exl-id: 3927d626-db16-4d30-80d3-5f63c3e9a110
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverから画像を読み込む際に使用する画像形式を指定します。 末尾が<span class="codeph"> -alpha</span>の形式を指定すると、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 コンポーネントの背景は、デフォルトで白です。 したがって、透明にするには、CSSの<span class="codeph"> background-color</span>プロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
