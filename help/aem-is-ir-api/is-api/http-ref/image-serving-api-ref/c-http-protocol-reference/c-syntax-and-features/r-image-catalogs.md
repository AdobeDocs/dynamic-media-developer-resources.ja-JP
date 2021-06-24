---
description: 画像カタログの機能と構文については、この節で説明します。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

画像カタログの機能と構文については、この節で説明します。

画像カタログには次の機能があります。

* 特定のメタデータおよび修飾子コマンドとの画像の永続的な関連付けを許可します。

   画像カタログ内のエントリは、ショートカット表記`*`rootId/objId`*`を使用して参照されます。ここで、`*`rootId`*`は画像カタログを、`*`objId`*`はカタログ内のデータレコードを表します。
* JPEG画質や透かしを適用するかどうかなど、特定の要求属性のデフォルトを指定します。
* フォント、ICCプロファイル、マクロ定義、および要求テンプレートの管理

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能はデフォルトのカタログ( [!DNL default.ini] )を使用して使用できます。

リクエストのURLパス内の`*`rootId`*`が特定の画像カタログの`attribute::RootId`と一致する場合、そのカタログがこのリクエストのメインカタログになります。 メインカタログには、リクエスト全体のデフォルトの属性と設定が表示されます。 一致が見つからない場合は、代わりにデフォルトのカタログが使用されます。

`src=`または`mask=`コマンドで識別されるカタログは、現在の画層に次のカタログ属性とデータを提供します。

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性/データ</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> 現在のレイヤ内のすべてのイメージファイルパスのデフォルトの拡張子 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> <span class="codeph">カタログのデフォルト：：有効期限</span>、またはカタログレコードが含まれていない場合は現在の画層の有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> 要求または現在のレイヤーに対する作業用ICCカラープロファイル、レンダリングインテント、ブラックポイント補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 現在の画層のすべてのソースファイルパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> <span class="codeph">カタログのデフォルト：:Resolution</span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> 現在のレイヤーの<span class="codeph"> anchor=</span>値のデフォルト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> すべてのレイヤーの最小の有効期限値が、返信画像の有効期限値として使用されます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 現在の画層のソースイメージカラープロファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 現在の画層の画像マップデータ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 現在のレイヤの<span class="codeph"> mask=</span>のデフォルト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 現在のレイヤのプレフィックスコマンド（同じレイヤに対して指定されている場合、 <span class="codeph"> catalog::Modifier</span>内の各コマンドは、URL内の同じコマンドで上書きできます） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 現在のレイヤのソースイメージファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 現在の画層の接尾記号コマンド（<span class="codeph"> catalog::Modifier</span>と似ていますが、 <span class="codeph"> catalog::PostModifier</span>内のコマンドは、URLまたは<span class="codeph"> catalog::Modifier</span>内で指定された同じコマンドを上書きします） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 現在の画層のオブジェクト解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内で、`src=`と`mask=`は同じ画像カタログ（存在する場合）を参照する必要があります。

`icc=`コマンドで識別されるカタログは、カタログのICCプロファイルテーブルからエントリを検索する目的でのみ使用されます。 他のカタログ属性やデータは関与しません。

`*`rootId`*`がカタログに解決され、`*`objId`*`がこのカタログの`catalog::Id`と一致する場合、 `*`rootId/objId`*`は、次のように、実際にカタログエントリに置き換えられます。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
