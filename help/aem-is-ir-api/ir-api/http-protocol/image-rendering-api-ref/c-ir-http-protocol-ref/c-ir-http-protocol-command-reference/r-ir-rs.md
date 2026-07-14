---
title: rs
description: 高度なレンダリング設定。 現在の選択範囲をレンダリングする際に適用する詳細なレンダリング設定を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
TQID: 'https://experienceleague.adobe.com/-wOy--XUu7TX6-rwrUFpuqz82bOwb4wpA9Pa0pM8J-4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 5%

---

# rs{#rs}

高度なレンダリング設定。 現在の選択範囲をレンダリングする際に適用する詳細なレンダリング設定を指定します。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>レンダリング設定文字列。 </p></td> 
 </tr> 
</table>

レンダリングの外観を微調整するために使用します。 レンダリング設定の文字列を作成するには、ビネット オーサリングツール（Dynamic Media画像オーサリングパッケージの一部）のレンダリング機能を使用します。

## プロパティ {#section-9a2b2228789046658cb80eddf343af75}

マテリアル属性：

## 初期設定 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 例 {#section-47e4811882574441a4d517e42a35f352}

画像オーサリングの一部の実験を行った後、アンシャープマスク（USM）によって、特定のアプリケーションとマテリアルに対して適切な量のシャープ処理が提供されると判断されます。 USMを構成するレンダリング設定文字列は、このマテリアルで使用する`rs=` コマンドにコピーされます。

`…&rs=U2V20W50X2&…`

## 関連項目 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)

