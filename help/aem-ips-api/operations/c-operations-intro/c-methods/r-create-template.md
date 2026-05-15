---
description: 複数のテキストレイヤーと画像レイヤーを持つことができるレイヤー画像を作成します。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 9%

---

# createTemplate{#createtemplate}

複数のテキストレイヤーと画像レイヤーを持つことができるレイヤー画像を作成します。

`urlModifier` パラメーターは、URLでユーザーが指定したコマンドの前に適用された、Image Server カタログに保存されているImage Server プロトコルコマンドを指定します。 `urlPostApplyModifier` パラメーターは、URL コマンドの後に適用されるプロトコルコマンドを指定します。このコマンドは、競合するユーザー指定の設定を上書きします。

## 承認済みユーザータイプ {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**入力（createTemplateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | テンプレートが属する会社。 |
| folderHandle | `xsd:string` | はい | テンプレートが格納されているフォルダーを表すフォルダーハンドル。 |
| name | `xsd:string` | はい | テンプレート名： |
| タイプ | `xsd:string` | はい | テンプレートタイプ： |
| urlModifier | `xsd:string` | はい | URLに対してユーザーが指定したコマンドの前に適用される、IS カタログに保存されているImage Server コマンドを指定します。 |
| urlPostApplyModifier | `xsd:string` | いいえ | URL コマンドの後に適用されるプロトコルコマンドを指定します。このコマンドは、競合するユーザー指定の設定を上書きします。 |

**出力（createTemplateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | テンプレートへのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコードのサンプルでは、ハンドルで指定されたフォルダーに、名前`APIcreateTemplate`、名前`urlModifier`、および`urlPostApplyModifier`のテンプレートを作成します。 応答は、新しく作成したテンプレートにハンドルを返します。

**リクエスト**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**応答**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
