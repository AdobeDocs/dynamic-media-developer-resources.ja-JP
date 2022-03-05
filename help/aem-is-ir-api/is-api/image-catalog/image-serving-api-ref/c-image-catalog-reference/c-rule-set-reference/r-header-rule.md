---
description: HTTP 応答ヘッダー要素。 のオプション <rule> 要素。
solution: Experience Manager
title: ヘッダ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# ヘッダ{#header}

HTTP 応答ヘッダー要素。 のオプション `<rule>` 要素。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*テキスト*&quot;** :必須。 HTTP ヘッダーの名前を指定します。

**`Action`= &quot;set&quot; |`"add"`**:オプション。 デフォルトはです。 `"set"`：現在のヘッダー値を置き換えます。 指定 `"add"` ヘッダー値を追加する場合は、コンマで区切ります。

## データ {#section-a387f541396c49d99c29692a38032914}

ヘッダー値。

## 説明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

新しい HTTP 応答ヘッダーの追加と、事前定義済みヘッダーの値の追加または置換を許可します。 名前と値は HTTP 標準に準拠している必要があります。 追加のエンコーディングは適用されません。

画像サービングの置き換え変数は、ヘッダー名とヘッダー値に使用できます。 これにより、リクエストから両方の文字列を制御できます。

## 例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

次のルールは、リクエストでヘッダー値が変数として指定されている場合、カスタムヘッダーを適用します。

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

このルールは、次のリクエスト（HTTP 応答ヘッダーを設定）によってトリガーされます。 `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
