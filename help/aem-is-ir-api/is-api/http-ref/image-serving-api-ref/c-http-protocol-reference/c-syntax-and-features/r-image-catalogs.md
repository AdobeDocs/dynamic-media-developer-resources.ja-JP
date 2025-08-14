---
description: この節では、画像カタログの機能と構文について説明します。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

この節では、画像カタログの機能と構文について説明します。

画像カタログには、次の機能が用意されています。

* 特定のメタデータおよび修飾子コマンドを使用して、画像を永続的に関連付けることができます。

  画像カタログのエントリは、ショートカット表記 `*`rootId/objId`*` を使用して参照されます。ここで `*`rootId`*` は画像カタログを識別し、`*`objId`*` はカタログ内のデータレコードを識別します。
* JPEGの品質や透かしを適用するかどうかなど、特定のリクエスト属性のデフォルトを指定します。
* フォント、ICC プロファイル、マクロ定義およびリクエストテンプレートの管理

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能はデフォルトのカタログ（[!DNL default.ini]）を介して使用できます。

リクエストの URL パスの `*`rootId`*` が特定の画像カタログの `attribute::RootId` と一致する場合、そのカタログがこのリクエストのメインカタログになります。 メインカタログには、リクエスト全体のデフォルトの属性と設定が用意されています。 一致するものが見つからない場合、代わりにデフォルトのカタログが使用されます。

`src=` または `mask=` コマンドで識別されるカタログは、次のカタログ属性とデータを現在の画層に提供します。

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性/データ </b> </th> 
   <th class="entry"> <b> Notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> 現在のレイヤーのすべての画像ファイルパスのデフォルトの拡張子 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Expiration</span> </p> </td> 
   <td> <p> カタログ <span class="codeph"> デフォルト：:Expiration</span> またはカタログレコードが含まれていない場合の現在のレイヤーの有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Icc*</span> </p> </td> 
   <td> <p> リクエストまたは現在のレイヤーの作業用 ICC カラープロファイル、レンダリングインテント、ブラックポイント補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:RootPath</span> </p> </td> 
   <td> <p> 現在のレイヤーのすべてのソースファイルのパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Resolution</span> </p> </td> 
   <td> <p> カタログ <span class="codeph"> デフォルト：:Resolution</span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> 現在のレイヤーの <span class="codeph"> anchor=</span> 値のデフォルト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> すべてのレイヤーの最小の有効期限値が、返信画像の有効期間の値として使用されます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像のカラープロファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 現在の画層のイメージ マップ データ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 現在のレイヤ <span class="codeph"> マスク=</span> のデフォルト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 現在の画層のプレフィクス コマンド（カタログ：:Modifier 内の各コマンド <span class="codeph"> は、同じ画層に対して指定されてい </span> 場合、URL 内の同じコマンドによって上書きできます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 現在の画層の接尾辞コマンド（カタログ：:Modifier<span class="codeph"> 似ていますが </span> カタログ：:PostModifier<span class="codeph"> のコマンド </span> は、URL またはカタログ：:Modifier で指定された同じコマンド <span class="codeph"> 上書きします） </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 現在の画層のオブジェクト解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内で、`src=` と `mask=` は同じ画像カタログ（存在する場合）を参照する必要があります。

`icc=` コマンドで識別されるカタログは、カタログの ICC プロファイルテーブルからエントリを検索するためにのみ使用されます。 他のカタログ属性やデータは含まれません。

`*`rootId`*` がカタログに解決され、`*`objId`*` がこのカタログ内の `catalog::Id` と一致した場合、`*`rootId/objId`*` は実質的に次のようなカタログエントリに置き換えられます。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[ 画像カタログ参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
