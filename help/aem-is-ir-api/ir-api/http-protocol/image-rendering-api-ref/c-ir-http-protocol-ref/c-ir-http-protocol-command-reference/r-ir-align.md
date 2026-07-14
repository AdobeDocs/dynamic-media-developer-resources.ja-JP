---
title: 整列
description: テクスチャ レンダリングの整列。 選択したビネット オブジェクトで定義されている原点のうち、使用する原点を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
TQID: 'https://experienceleague.adobe.com/U6V-e23e9ILdnQfTpJzGPzbCTZEICccSpcMebA-NRjA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 4%

---

# 整列 {#align}

テクスチャ レンダリングの整列。 選択したビネット オブジェクトで定義されている原点のうち、使用する原点を指定します。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>デフォルトの（center-match）オリジン。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>継続的なマッチングの開始： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>ランダムな整列： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>ユーザー定義のオリジン： </p></td> 
 </tr> 
</table>

レンダラーは、テクスチャアンカーポイント（`anchor=`）が指定された原点と一致するように、テクスチャをオブジェクトに適用します。

各オブジェクトは、最大6つの原点（0、1、3、4、5、6）を定義できます。 `align`値が指定されていても、対応する原点がビネットオブジェクトで定義されていない場合は、デフォルトの（center-match）原点が使用されます。

`align=2` ランダムなテクスチャの配置を指定します。この場合、`anchor=`は効果的に無視されます。

主に室内装飾品の材料に使用され、おそらくアパレル生地に使用され、隣接するオブジェクト間のテクスチャの整列を管理します。

## プロパティ {#section-350fadc87dcf4812a8a02d1c3d6697a0}

マテリアル属性： 壁、キャビネット、アプライアンス、または窓のカバー枠オブジェクトが選択されている場合、またはマテリアルが繰り返し可能なテクスチャではない場合は無視されます。

## 初期設定 {#section-3231c2854bae4477836b626ac208dd34}

マテリアルがカタログ エントリに基づいている場合は`catalog::Alignment`、そうでない場合は0 （center-matched）。

## 関連項目 {#section-945d1ce275df487d9d564d4043156c79}

[&#x200B; カタログ：：線形](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399)、[&#x200B; アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

