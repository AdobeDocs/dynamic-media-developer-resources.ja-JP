---
description: フラグを適用します。 追加のレンダリングオプションを指定します。
solution: Experience Manager
title: フラグ
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '78'
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

`flags=0` （デフォルト）上部キャビネットをソリッドドアでレンダリングします。

`flags=1` は、ガラスのドアが付いた上部キャビネットをレンダリングします（ビネットがガラスのドアでオーサリングされている場合）。

## プロパティ {#section-a2b00d7bb15e449ea85178acb92d8285}

マテリアル属性 キャビネットマテリアル以外の場合、またはターゲットキャビネットオブジェクトでガラスのドアが許可されていない場合は無視されます。

## 初期設定 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` ガラスの扉はない
