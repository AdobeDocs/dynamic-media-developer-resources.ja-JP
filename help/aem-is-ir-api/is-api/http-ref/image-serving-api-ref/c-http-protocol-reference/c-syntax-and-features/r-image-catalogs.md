---
description: この節では、画像カタログの機能と構文について説明します。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
TQID: 'https://experienceleague.adobe.com/Q4n6YZ31shF1ZAGUwbg6Q7ovYNT9b3K1MCaovmKBmAo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 476
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

この節では、画像カタログの機能と構文について説明します。

画像カタログには、次の機能があります。

* 特定のメタデータおよび修飾子コマンドを使用して、画像を永続的に関連付けることができます。

  画像カタログのエントリは、ショートカット表記`*`rootId/objId`*`を使用して参照されます。ここで、`*`rootId`*`は画像カタログを識別し、`*`objId`*`はカタログ内のデータレコードを識別します。
* JPEGの画質や透かしを適用するかどうかなど、特定のリクエスト属性にデフォルトを指定します。
* フォント、ICC プロファイル、マクロ定義、リクエストテンプレートの管理

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能は、デフォルトカタログ（[!DNL default.ini]）を介して利用できます。

リクエストのURL パスの`*`rootId`*`が特定の画像カタログの`attribute::RootId`と一致する場合、そのカタログがこのリクエストのメインカタログになります。 メインカタログには、リクエスト全体のデフォルトの属性と設定が用意されています。 一致するものが見つからない場合は、代わりにデフォルトカタログが使用されます。

`src=`または`mask=` コマンドで識別されたカタログは、次のカタログ属性とデータを現在のレイヤーに提供します。

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>属性/データ </b> </th> 
   <th class="entry"> <b>件のメモ </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">属性：:DefaultExt</span> </p> </td> 
   <td> <p> 現在のレイヤー内のすべての画像ファイルパスのデフォルトの拡張子 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：有効期限</span> </p> </td> 
   <td> <p> <span class="codeph"> カタログの既定値：：有効期限</span>、またはカタログ レコードが含まれていない場合の現在のレイヤーの有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:Icc*</span> </p> </td> 
   <td> <p> リクエストおよび/または現在のレイヤーの有効なICC カラープロファイル、レンダーインテント、およびblackpoint補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:RootPath</span> </p> </td> 
   <td> <p> 現在のレイヤーのすべてのソースファイルパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：解像度</span> </p> </td> 
   <td> <p> <span class="codeph"> カタログの既定：：解像度</span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：アンカー</span> </p> </td> 
   <td> <p> 現在のレイヤーの<span class="codeph"> アンカー=</span>値の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：有効期限</span> </p> </td> 
   <td> <p> すべてのレイヤーの最小有効期限値は、返信画像の有効期間の値として使用されます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:IccProfile</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像カラープロファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:Map</span> </p> </td> 
   <td> <p> 現在のレイヤーの画像マップデータ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:MaskPath</span> </p> </td> 
   <td> <p> 現在のレイヤーの<span class="codeph"> マスク=</span>の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：修飾子</span> </p> </td> 
   <td> <p> 現在のレイヤーの接頭辞コマンド（<span class="codeph"> カタログ：:Modifier</span>の各コマンドは、同じレイヤーに指定されている場合、URLで同じコマンドで上書きできます） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：パス </span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:PostModifier</span> </p> </td> 
   <td> <p> 現在のレイヤーのpostfix コマンド（<span class="codeph"> カタログ：:Modifier</span>と同様ですが、<span class="codeph"> カタログ：:PostModifier</span>のコマンドは、URLまたは<span class="codeph"> カタログ：:Modifier</span>で指定されたコマンドと同じコマンドを上書きします） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：解像度</span> </p> </td> 
   <td> <p> 現在のレイヤーのオブジェクトの解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内で、`src=`と`mask=`は同じ画像カタログを参照する必要があります（存在する場合）。

`icc=` コマンドで識別されたカタログは、カタログのICC プロファイルテーブルからエントリを検索するためにのみ使用されます。 他のカタログ属性やデータは含まれません。

`*`rootId`*`がカタログに解決し、`*`objId`*`がこのカタログの`catalog::Id`と一致する場合、`*`rootId/objId`*`は実質的に次のようになります。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[&#x200B; マスク=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[&#x200B; アンカー=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
