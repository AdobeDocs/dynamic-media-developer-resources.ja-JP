---
description: XMPメタデータ： リクエストパスで指定された画像に関連付けられているXMP メタデータを返します。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
TQID: 'https://experienceleague.adobe.com/yPJzG9VRk975dHWzRc6o-OX5njAccH8CcwpR-J--uHk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 2%

---

# xmp{#xmp}

XMPメタデータ： リクエストパスで指定された画像に関連付けられているXMP メタデータを返します。

`req=xmp`

他のコマンドは無視されます。 UTF-8 エンコーディングが適用されます。 応答は、MIME タイプ `text/xml`を持つXMLとしてフォーマットされます。

HTTP応答は、`catalog::Expiration`に基づくTTLでキャッシュできます。

## プロパティ {#section-0d26b6a56c844153ae5cea4880370d00}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

URLに画像パスまたは修飾子が含まれていない場合は、次の手順を実行します。

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外は、`req=img`

## 例 {#section-34213692deab4a0f9037d5844132ee14}

画像ファイルのプロパティをクエリします。

` http:// *` サーバー`*/myPath/myImage.tif?req=imageprops`

クエリ画像カタログのプロパティ：

` http:// *` サーバー`*/myRootId?req=catalogprops`

HTML ファイルに埋め込まれたクライアントサイドのJavaScriptから、画像カタログエントリのプロパティにアクセスします。

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

特定のカタログエントリのマスク画像を、元のサイズの25%に拡大/縮小して取得します。

` http:// *` サーバー`*/myRootId/myImageId?req=mask&scale=0.25`

画像を1/8のサイズでリクエストする：

` http:// *` サーバー`*/myRootId/myImageId?scl=8`

これは次と同じです。

` http:// *` サーバー`*/myRootId/myImageId?req=img&scl=8`

画像カタログで指定されたサムネール属性に基づいて、画像のサムネールをリクエストします。

` http:// *` サーバー`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

サーバーログにテキストメッセージを送信します。

` http:// *` サーバー`*/myRootId?req=message&message=This%20is%20the%20message`

## 関連項目 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[ カタログ：：ターゲット ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)、[ カタログ：:UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)、[ サムネール拡大・縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)、[ プロパティ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)、[画像マップ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
