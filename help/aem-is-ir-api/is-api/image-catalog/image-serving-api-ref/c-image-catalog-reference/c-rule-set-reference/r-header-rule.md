---
description: HTTP応答ヘッダー要素。 <rule>要素のオプションです。
solution: Experience Manager
title: ヘッダ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# ヘッダ{#header}

HTTP応答ヘッダー要素。 `<rule>`要素ではオプションです。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必須。HTTPヘッダーの名前を指定します。

**`Action`= &quot;set&quot; |`"add"`**:オプション。初期設定は`"set"`で、現在のヘッダー値を置き換えます。 `"add"`を指定して、ヘッダー値をコンマで区切ります。

## データ {#section-a387f541396c49d99c29692a38032914}

ヘッダー値。

## 説明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

新しいHTTP応答ヘッダーの追加と、事前定義済みヘッダーの値の追加または置き換えを可能にします。 名前と値は、HTTP標準に準拠している必要があります。 追加のエンコーディングは適用されません。

ヘッダー名とヘッダー値には、画像サービングの置き換え変数を使用できます。 これにより、リクエストから両方の文字列を制御できます。

## 例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

次のルールは、リクエストでヘッダー値が変数として指定されている場合、カスタムヘッダーを適用します。

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

このルールは、HTTP応答ヘッダー`Edge-Control::no-store`を設定する次のリクエストによってトリガーされます。

`http://server/is/image/cat/id?$Edge-Control=no-store`
