---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> ヒントテキストが非表示になるまでの秒数を指定します。 <span class="codeph"> -1</span>に設定すると、ユーザがフライアウトをアクティブにした場合でも、メッセージが常に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> セット内の新しい画像を表示する際に、テキストが表示される回数を指定します。 値<span class="codeph"> -1</span>は、セット内の画像を表示する際に、テキストが常に表示されることを意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> テキストを表示または非表示にするときに行うフェードアニメーションの時間を指定します。 値<span class="codeph"> 0</span>は、フェードトランジションがないことを示します。 </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
