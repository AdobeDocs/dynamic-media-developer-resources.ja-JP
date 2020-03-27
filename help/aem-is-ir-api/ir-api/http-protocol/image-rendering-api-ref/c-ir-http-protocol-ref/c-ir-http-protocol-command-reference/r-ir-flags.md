---
description: フラグを適用します。 追加のレンダリングオプションを指定します。
seo-description: フラグを適用します。 追加のレンダリングオプションを指定します。
seo-title: フラグ
solution: Experience Manager
title: フラグ
topic: Scene7 Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

`flags=1` ビネットがガラスドアでオーサリングされている場合は、上部キャビネットをガラスドアでレンダリングします。

## プロパティ {#section-a2b00d7bb15e449ea85178acb92d8285}

マテリアル属性。 キャビネットの材料でない場合、またはターゲットのキャビネットオブジェクトでガラスのドアが許可されていない場合は無視されます。

## 初期設定 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` ガラスの扉はない
