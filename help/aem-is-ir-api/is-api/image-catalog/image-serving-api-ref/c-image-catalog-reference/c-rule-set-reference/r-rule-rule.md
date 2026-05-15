---
title: ルール
description: リクエストルール要素： <ruleset>要素では、1つ以上のルールがオプションです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
TQID: 'https://experienceleague.adobe.com/Cb5DzbRJBDdUEt-daR36rT6CRPMkclg0KtU47IdzWik'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 2%

---

# ルール{#rule}

リクエストルール要素： `<ruleset>`要素では、1つ以上のルールがオプションです。

## 属性 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: オプション。 デフォルトは「break」です。

`Replace = "first" | "all"`: オプション。 デフォルトは「first」です。

`RequestType` = *&quot;`types`&quot;*: オプション。 ルールが適用される入力コンテキストを指定します。 *`types`*&#x200B;はコンマ区切りのリストです。次の表に示す1つ以上のトークンを含めることができます。 `RequestType`が指定されていない場合、ルールは、サポートされているすべてのコンテキストで受信したリクエストに適用されます。

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b> トークン </b> </p> </th> 
   <th class="entry"> <p><b> コンテキスト </b> </p> </th> 
   <th class="entry"> <p><b>説明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">は</span>です </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>画像サービングリクエストに適用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>画像レンダリングリクエストに適用 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">静的</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>静的コンテンツリクエストに適用 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: オプション。 デバッグログとエラーメッセージで`<rule>`要素を識別するために使用します。

`  *`属性`* ="value"`: オプション。 `<rule>`要素は、任意の組み合わせで次のいずれかの属性を定義できます。 指定され、ルールが正常に一致した場合、このリクエストに対応するカタログ属性が上書きされます。 デフォルトは`RequestType="is"`です。

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname">属性</span> </b> </th> 
   <th class="entry"> <p>対応する画像カタログ属性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local">属性：:DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local">属性：:ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">有効期限</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local">属性：：有効期限</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local">属性：:MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local">属性：:RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local">属性：:RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local">属性：:RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local">属性：:SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local">属性：:WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

詳しくは、対応する画像カタログ属性の説明を参照してください。

有効期限の属性は、デフォルトの属性値のみを上書きします。 特定の`catalog::Expiration`値がリクエストに適用される場合、上書きは無視されます。

## データ {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;式&gt;</span> </p></td> 
  <td class="stentry"> <p>オプション </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;代替&gt;</span> </p></td> 
  <td class="stentry"> <p>オプション </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>オプション </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>オプション </p></td> 
 </tr> 
</table>

## 説明 {#section-0c5fbc363070419d8c9800b0c02dc9f9}

`<expression>`と`<substitution>`の両方が指定されていて、キャプチャされた部分文字列が使用されていない場合、最初に一致した部分文字列は`<substitution>`に置き換えられます。

`<expression>`が指定されていない場合、パスが一致し、`<substitution>`がパスの末尾に追加されます。

`<substitution>`が指定されていない場合、パスまたはクエリの変換は行われませんが、指定されたカタログ属性は上書きされます。 `<substitution>`が空の場合、一致する部分文字列は削除されます。

`<addressfilter>`は、一致が発生し、クエリ ルールが適用される前にのみ適用されます。
