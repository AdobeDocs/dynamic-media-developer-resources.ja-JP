---
description: フラグを適用します。 追加のレンダリングオプションを指定します。
solution: Experience Manager
title: フラグ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# フラグ{#flags}

フラグを適用します。 追加のレンダリングオプションを指定します。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>フラグの値。 </p></td> 
 </tr> 
</table>

現在はキャビネットの材料にのみ使用されています。

`flags=0` （既定）は、ソリッドドアを持つ上部キャビネットをレンダリングします。

`flags=1` は、ガラスのドアを持つ上部キャビネットをレンダリングします（ビネットがガラスのドアでオーサリングされている場合）。

## プロパティ {#section-a2b00d7bb15e449ea85178acb92d8285}

マテリアル属性。 キャビネットマテリアルでない場合や、ターゲットキャビネットオブジェクトでガラスドアが許可されていない場合は無視されます。

## 初期設定 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` ガラスの扉はない
