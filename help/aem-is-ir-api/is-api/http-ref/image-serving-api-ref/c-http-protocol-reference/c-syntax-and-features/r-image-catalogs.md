---
description: 画像カタログの機能と構文については、この節で説明します。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

画像カタログの機能と構文については、この節で説明します。

画像カタログには次の機能があります。

* 特定のメタデータおよび修飾子コマンドを使用して、画像の永続的な関連付けを許可します。

   画像カタログ内のエントリは、ショートカット表記を使用して参照されます `*`rootId/objId`*`で、 `*`rootId`*` は画像カタログを識別し、 `*`objId`*` カタログ内のデータレコードを識別します。
* 特定の要求属性のデフォルト (JPEGの品質や透かしを適用するかどうかなど ) を指定します。
* フォント、ICC プロファイル、マクロ定義、要求テンプレートを管理します

特定の画像カタログが定義されていない場合でも、画像カタログのすべての機能はデフォルトのカタログ ( [!DNL default.ini]) をクリックします。

If `*`rootId`*` の URL パスが一致する `attribute::RootId` 特定の画像カタログの場合、そのカタログがこのリクエストのメインカタログになります。 メインカタログには、要求全体のデフォルトの属性と設定が表示されます。 一致するものが見つからない場合は、代わりにデフォルトのカタログが使用されます。

カタログが `src=` または `mask=` コマンドは、現在の画層に次のカタログ属性とデータを提供します。

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
   <td> <p> 現在のレイヤー内のすべてのイメージファイルパスのデフォルトの拡張子 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> デフォルト <span class="codeph"> catalog::Expiration</span> カタログレコードが関係しない場合は、現在の画層の有効期限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> 要求または現在のレイヤーに対する作業用 ICC カラープロファイル、レンダリングインテント、黒点補正フラグ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 現在の画層のすべてのソースファイルパスに使用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> デフォルト <span class="codeph"> catalog::Resolution</span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> デフォルト <span class="codeph"> anchor=</span> 現在の画層の値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> すべてのレイヤーの最小の有効期限値が、返信画像の有効期限値として使用されます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 現在の画層のソース画像カラープロファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 現在の画層の画像マップデータ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> デフォルト <span class="codeph"> mask=</span> 現在の画層の </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 現在の画層のプレフィックスコマンド ( <span class="codeph"> catalog::Modifier</span> は、同じレイヤーに対して指定されている場合、URL 内の同じコマンドで上書きできます ) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 現在の画層のソース画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 現在の画層の postfix コマンド ( <span class="codeph"> catalog::Modifier</span>のコマンド以外に <span class="codeph"> catalog::PostModifier</span> URL または <span class="codeph"> catalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 現在の画層のオブジェクト解像度 </p> </td> 
  </tr> 
 </tbody> 
</table>

同じレイヤー内で、 `src=` および `mask=` は、同じ画像カタログを参照する必要があります（存在する場合）。

カタログが `icc=` コマンドは、カタログの ICC プロファイルテーブルからエントリを検索する目的でのみ使用します。 他のカタログ属性やデータは関係ありません。

もし `*`rootId`*` カタログに解決され、 `*`objId`*` が `catalog::Id` このカタログでは、 `*`rootId/objId`*` は、次のようなカタログエントリに事実上置き換えられます。

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 関連項目 {#section-00e4f6b39cd14244bcce537a3f831259}

[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
