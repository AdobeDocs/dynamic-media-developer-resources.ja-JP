---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
TQID: 'https://experienceleague.adobe.com/RAxn-9VY1W6XWau-hMwdiiIks9Fzdrtex0C54aHs-tE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`期間`*[, *` カウント `*][, *` フェード `*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">期間</span> </span> </p> </td> 
   <td colname="col2"> <p>ヒント テキストが非表示になる前に表示される秒数を指定します。 <span class="codeph"> -1</span>に設定すると、ユーザーがフライアウトをアクティブにした場合でも、メッセージは常に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> カウント </span> </span> </p> </td> 
   <td colname="col2"> <p>セット内の新しい画像を表示する際に、テキストが表示される回数を指定します。 値<span class="codeph"> -1</span>は、セット内の任意の画像を表示する際に、テキストが常に表示されることを意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> フェード </span> </span> </p> </td> 
   <td colname="col2"> <p>テキストが表示または非表示になったときに発生するフェードアニメーションのデュレーションを指定します。 値<span class="codeph"> 0</span>は、フェード遷移がないことを意味します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
