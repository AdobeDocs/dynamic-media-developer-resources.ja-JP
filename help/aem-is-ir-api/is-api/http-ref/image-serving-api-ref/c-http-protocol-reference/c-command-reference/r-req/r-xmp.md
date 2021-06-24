---
description: XMPメタデータ。 リクエストパスで指定された画像に関連付けられたXMPメタデータを返します。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 6%

---

# xmp{#xmp}

XMPメタデータ。 リクエストパスで指定された画像に関連付けられたXMPメタデータを返します。

`req=xmp`

その他のコマンドは無視されます。 UTF-8エンコーディングが適用されます。 応答は、MIMEタイプ`text/xml`のXML形式です。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

## プロパティ {#section-0d26b6a56c844153ae5cea4880370d00}

リクエスト属性。 現在の画層設定に関係なく適用されます。

## 初期設定 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

URLに画像パスや修飾子が含まれていない場合：

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外の場合は、`req=img`

## 例 {#section-34213692deab4a0f9037d5844132ee14}

クエリ画像ファイルのプロパティ。

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

クエリ画像カタログのプロパティ：

` http:// *`server`*/myRootId?req=catalogprops`

HTMLファイルに埋め込まれたクライアント側JavaScriptから、画像カタログエントリのプロパティにアクセスします。

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

特定のカタログエントリのマスク画像を取得し、元のサイズの25%に拡大/縮小します。

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

8分の1のサイズの画像をリクエストします。

` http:// *`server`*/myRootId/myImageId?scl=8`

これは、次と同じです。

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

画像のサムネールを要求します。画像カタログで指定されたサムネール属性に基づきます。

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

サーバーログにテキストメッセージを送信します。

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## 関連項目 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 、 [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)、 [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)、 [サムネールの拡大/縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)、 [プロパティ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)、 [画像マップ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
