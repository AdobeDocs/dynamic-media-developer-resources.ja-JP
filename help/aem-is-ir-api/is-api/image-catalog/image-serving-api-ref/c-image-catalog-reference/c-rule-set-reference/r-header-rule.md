---
title: ヘッダ
description: HTTP応答ヘッダー要素。 <rule>要素ではオプションです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: 'https://experienceleague.adobe.com/-hGRn7zVjm8eavZIwBoiAuCqoSNYIFSSlQaSP6wuHXs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 2%

---

# ヘッダ{#header}

HTTP応答ヘッダー要素。 `<rule>`要素ではオプションです。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**：必須。 HTTP ヘッダーの名前を指定します。

**`Action`= &quot;set&quot; |`"add"`**: オプション。 デフォルトは`"set"`で、現在のヘッダー値が置き換えられます。 ヘッダー値をコンマで区切って追加できるように、`"add"`を指定します。

## データ {#section-a387f541396c49d99c29692a38032914}

ヘッダー値。

## 説明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

新しいHTTP応答ヘッダーを追加したり、定義済みのヘッダーの値を追加または置き換えたりできます。 名前と値はHTTP標準に準拠している必要があります。 追加のエンコーディングは適用されません。

画像サービング代用変数は、ヘッダー名とヘッダー値で使用できます。 これにより、リクエストから両方の文字列を制御できます。

## 例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

次のルールは、ヘッダー値がリクエストで変数として指定された場合にカスタムヘッダーを適用します。

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

このルールは、HTTP応答ヘッダー`Edge-Control::no-store`を設定する次のリクエストによってトリガーされます。

`http://server/is/image/cat/id?$Edge-Control=no-store`
