---
description: この節では、画像カタログの機能と構文について説明します。
seo-description: この節では、画像カタログの機能と構文について説明します。
seo-title: 画像カタログ
solution: Experience Manager
title: 画像カタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像カタログ{#image-catalogs}

この節では、画像カタログの機能と構文について説明します。

画像カタログには、次の機能があります。

* 画像と特定のメタデータおよび修飾子コマンドとの永続的な関連付けを許可します。

   画像カタログ内のエントリは、 ` *`rootId/objId`*`( ` *`rootIdは画像カタログを、`*`` *``*` objIdはカタログ内のデータレコードを示す)のショートカット表記を使用して参照されます。
* JPEG画質や透かしを適用するかどうかなど、特定の要求属性のデフォルトを指定します。
* フォント、ICCプロファイル、マクロ定義、および要求テンプレートの管理

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能は、初期設定のカタログ( [!DNL default.ini])を介して使用できます。

リクエ ` *`ストの`*` URLパスのrootIdが特定の画像カタログと一致する `attribute::RootId` 場合、そのカタログはこのリクエストのメインカタログになります。 メインカタログは、リクエスト全体のデフォルトの属性と設定を提供します。 一致が見つからない場合は、代わりにデフォルトのカタログが使用されます。

またはコマンドで識別されるカ `src=` タログ `mask=` は、次のカタログ属性とデータを現在の画層に提供します。

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
   <td> <p> 現在のレイヤー内のすべての画像ファイルパスの初期設定の拡張子 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> カタログ <span class="codeph"> ::Expiration</span> 、またはカタログレコードが含まれない場合の現在の画層の有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> 要求および/または現在のレイヤーの作業用ICCカラープロファイル、レンダリングインテント、ブラックポイント補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 現在の画層のすべてのソースファイルパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> カタログの <span class="codeph"> 初期設定：解像度</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> 初期設定のアンカー <span class="codeph"> =現在のレイ</span> ヤーの値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> すべてのレイヤーの最小の有効期限値が、返信画像の有効期限値として使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像のカラープロファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 現在のレイヤーの画像マップデータ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 現在のレイ <span class="codeph"> ヤーのmask=</span> の初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 現在の画層のプリフィックスコマンド(同じ画層に対して <span class="codeph"> catalog::Modifier</span> の各コマンドを指定した場合、URL内の同じコマンドで上書きできます) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 現在のレイヤーのソース画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 現在のレイヤーの接尾記号コマンド( <span class="codeph"> catalog::Modifier</span>に似ていますが、 <span class="codeph"> catalog::PostModifierのコマンドは、URLまたはcatalog</span> ::Modifierで指定された同じコマンドに優先 <span class="codeph"> します</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 現在のレイヤーのオブジェクト解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内にあり、同 `src=` じ画像カ `mask=` タログ（存在する場合）を参照する必要があります。

コマンドで識別されたカタ `icc=` ログは、カタログのICCプロファイルテーブルからエントリを検索する目的でのみ使用されます。 他のカタログ属性やデータは含まれません。

rootId ` *`がカタログに解決され、`*` objId ` *`がこのカタログ内のと一致する場合、`*` rootId/objId `catalog::Id`` *``*` は、次のようなカタログエントリによって実際に置き換えられます。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[、anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
