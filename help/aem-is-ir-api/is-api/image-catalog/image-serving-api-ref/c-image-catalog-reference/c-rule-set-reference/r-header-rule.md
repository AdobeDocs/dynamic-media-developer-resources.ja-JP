---
description: HTTP応答ヘッダー要素。 <rule>要素のオプションです。
seo-description: HTTP応答ヘッダー要素。 <rule>要素のオプションです。
seo-title: ヘッダ
solution: Experience Manager
title: ヘッダ
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ヘッダ{#header}

HTTP応答ヘッダー要素。 要素のオプシ `<rule>` ョンです。

## Attributes {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**:必須。 HTTPヘッダーの名前を指定します。

**`Action`= &quot;set&quot;|`"add"`**:オプション。 初期設定はで`"set"`、現在のヘッダー値がすべて置き換えられます。 ヘッダ`"add"`ー値をコンマで区切って追加する場合に指定します。

## データ {#section-a387f541396c49d99c29692a38032914}

ヘッダー値。

## 説明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

新しいHTTP応答ヘッダーの追加と、事前定義ヘッダーの値の追加または置換を許可します。 名前と値は、HTTP標準に準拠している必要があります。 追加のエンコーディングは適用されません。

画像サービング置換変数は、ヘッダー名とヘッダー値に使用できます。 これにより、リクエストの両方の文字列を制御できます。

## 例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

次のルールは、ヘッダー値が変数としてリクエストで指定されている場合に、カスタムヘッダーを適用します。

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

このルールは、次のリクエストでHTTP応答ヘッダーを設定することによってトリガーされま `Edge-Control::no-store`す。

`http://server/is/image/cat/id?$Edge-Control=no-store`
