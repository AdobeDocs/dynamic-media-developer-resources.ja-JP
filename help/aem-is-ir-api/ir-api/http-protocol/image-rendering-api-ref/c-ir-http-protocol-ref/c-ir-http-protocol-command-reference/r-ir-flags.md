---
title: フラグ
description: フラグを適用します。 追加のレンダリングオプションを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# フラグ {#flags}

フラグを適用します。 追加のレンダリングオプションを指定します。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>フラグ値。 </p></td> 
 </tr> 
</table>

現在、キャビネットの材料にのみ使用されています。

`flags=0` （既定）上部キャビネットをソリッド ドアでレンダリングします。

`flags=1` ガラスのドアを使用して上部キャビネットをレンダリングします（ガラスのドアを使用してビネットを作成した場合）。

## プロパティ {#section-a2b00d7bb15e449ea85178acb92d8285}

マテリアル アトリビュート。 キャビネット マテリアルでない場合、またはターゲットのキャビネット オブジェクトがガラス ドアを許可しない場合は無視されます。

## 初期設定 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` ガラス製のドアは不可。
