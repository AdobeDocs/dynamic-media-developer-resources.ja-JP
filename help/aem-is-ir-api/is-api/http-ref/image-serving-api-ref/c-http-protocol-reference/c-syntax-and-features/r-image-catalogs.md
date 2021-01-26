---
description: この節では、画像カタログの機能と構文について説明します。
seo-description: この節では、画像カタログの機能と構文について説明します。
seo-title: 画像カタログ
solution: Experience Manager
title: 画像カタログ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# 画像カタログ{#image-catalogs}

この節では、画像カタログの機能と構文について説明します。

画像カタログオファーには、次の機能があります。

* 画像と特定のメタデータおよび修飾子コマンドとの永続的な関連付けを許可します。

   画像カタログ内のエントリは、ショートカット表記`*`rootId/objId`*`を使用して参照されます。ここで`*`rootId`*`は画像カタログを、`*`objId`*`はカタログ内のデータレコードを示します。
* JPEG画質や透かしを適用するかどうかなど、特定の要求属性のデフォルトを指定します。
* フォント、ICCプロファイル、マクロ定義、および要求テンプレートの管理

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能は、初期設定のカタログ([!DNL default.ini])を介して使用できます。

リクエストのURLパス内の`*`rootId`*`が特定の画像カタログの`attribute::RootId`と一致する場合、そのカタログがこのリクエストのメインカタログになります。 メインカタログには、リクエスト全体のデフォルトの属性と設定が表示されます。 一致が見つからない場合は、代わりにデフォルトのカタログが使用されます。

`src=`または`mask=`コマンドで識別されるカタログは、次のカタログ属性とデータを現在の画層に提供します。

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
   <td> <p> 現在のレイヤー内のすべてのイメージファイルパスの初期設定の拡張子。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> <span class="codeph">カタログの初期設定：:Expiration</span>またはカタログレコードが含まれない場合は現在の画層の有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> リクエストおよび/または現在のレイヤーに対する作業中のICCカラープロファイル、レンダリングインテント、ブラックポイント補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 現在の画層のすべてのソースファイルパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> <span class="codeph">カタログの初期設定：:Resolution</span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> 現在のレイヤーの<span class="codeph"> anchor=</span>値の初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> すべてのレイヤーの最も小さい有効期限の値が、返信画像の有効期限の値として使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 現在のレイヤーのソースプロファイルのカラー画像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 現在のレイヤーの画像マップデータ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 現在のレイヤーの<span class="codeph"> mask=</span>の初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 現在のレイヤーのプリフィックスコマンド（<span class="codeph"> catalog::Modifier</span>の各コマンドは、同じレイヤーに対して指定されている場合、URL内の同じコマンドで上書きできます） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 現在のレイヤーの接尾記号コマンド（<span class="codeph"> catalog::Modifier</span>に似ていますが、<span class="codeph"> catalog::PostModifier</span>のコマンドは、URLまたは<span class="codeph"> catalog::Modifier</span>に指定された同じコマンドを上書きします） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 現在のレイヤーのオブジェクト解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内で、`src=`と`mask=`は、同じ画像カタログ（存在する場合）を参照する必要があります。

`icc=`コマンドで識別されるカタログは、カタログのICCプロファイルテーブルからエントリを検索する目的でのみ使用されます。 他のカタログ属性やデータは関係しません。

`*`rootId`*`がカタログに解決され、`*`objId`*`がこのカタログ内の`catalog::Id`と一致する場合、`*`rootId/objId`*`は、次のようなカタログエントリに効果的に置き換えられます。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[画像カタログリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
