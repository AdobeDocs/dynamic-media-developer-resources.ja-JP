---
description: HTTP応答ヘッダー要素。 <rule>要素のオプションです。
seo-description: HTTP応答ヘッダー要素。 <rule>要素のオプションです。
seo-title: ヘッダ
solution: Experience Manager
title: ヘッダ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# ヘッダ{#header}

HTTP応答ヘッダー要素。 `<rule>`要素のオプションです。

## 属性{#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必須。HTTPヘッダーの名前を指定します。

**`Action`= &quot;set&quot; |`"add"`**:オプション。初期設定は`"set"`で、現在のヘッダー値を置き換えます。 ヘッダー値を追加する場合は、`"add"`を指定し、カンマで区切ります。

## データ {#section-a387f541396c49d99c29692a38032914}

ヘッダー値。

## 説明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

新しいHTTP応答ヘッダーの追加、および事前定義のヘッダーの値の追加または置き換えを許可します。 名前と値は、HTTP標準に準拠している必要があります。 追加のエンコーディングは適用されません。

画像サービング置換変数は、ヘッダ名とヘッダ値に使用できます。 これにより、リクエストの両方の文字列を制御できます。

## 例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

次のルールは、ヘッダー値が変数として要求で指定されている場合に、カスタムヘッダーを適用します。

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

このルールは、次のリクエストによってトリガーされ、HTTP応答ヘッダー`Edge-Control::no-store`が設定されます。

`http://server/is/image/cat/id?$Edge-Control=no-store`
