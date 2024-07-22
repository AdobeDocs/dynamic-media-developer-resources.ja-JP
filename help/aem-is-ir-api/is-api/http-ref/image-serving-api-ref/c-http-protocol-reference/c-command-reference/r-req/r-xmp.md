---
description: XMP メタデータ。 リクエストパスで指定された画像に関連付けられたXMP メタデータを返します。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# xmp{#xmp}

XMP メタデータ。 リクエストパスで指定された画像に関連付けられたXMP メタデータを返します。

`req=xmp`

その他のコマンドは無視されます。 UTF-8 エンコーディングが適用されます。 応答は、MIME タイプ `text/xml` を持つ XML としてフォーマットされます。

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

## プロパティ {#section-0d26b6a56c844153ae5cea4880370d00}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。

## 初期設定 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

URL に画像のパスや修飾子が含まれていない場合は、次のようになります。

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外の場合は、`req=img`

## 例 {#section-34213692deab4a0f9037d5844132ee14}

クエリ画像ファイルのプロパティ。

` http:// *` サーバー `*/myPath/myImage.tif?req=imageprops`

クエリ画像カタログのプロパティ：

` http:// *` サーバー `*/myRootId?req=catalogprops`

HTMLファイルに埋め込まれたクライアントサイドのJavaScriptから、画像カタログエントリのプロパティにアクセスします。

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

特定のカタログエントリのマスク画像を取得します。このマスク画像は、元のサイズの 25% に拡大縮小されます。

` http:// *` サーバー `*/myRootId/myImageId?req=mask&scale=0.25`

8/1 サイズの画像をリクエストします。

` http:// *` サーバー `*/myRootId/myImageId?scl=8`

これは次と同じです。

` http:// *` サーバー `*/myRootId/myImageId?req=img&scl=8`

画像カタログで指定されたサムネール属性に基づいて、画像のサムネールをリクエストします。

` http:// *` サーバー `*/myRootId/myImageId?req=tmb&wid=64&hei=64`

サーバーログにテキストメッセージを送信します。

` http:// *` サーバー `*/myRootId?req=message&message=This%20is%20the%20message`

## 関連項目 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)、[catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)、[ サムネールの拡大縮小 ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)、[ プロパティ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)、[ 画像マップ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
