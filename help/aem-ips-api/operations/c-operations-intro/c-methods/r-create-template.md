---
description: 複数のテキストと画像レイヤーを含むレイヤーイメージを作成します。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 10%

---

# createTemplate{#createtemplate}

複数のテキストと画像レイヤーを含むレイヤーイメージを作成します。

`urlModifier`パラメーターは、URL上のユーザーが指定したコマンドの前に適用されるImage Serverカタログに保存されるImage Serverプロトコルコマンドを指定します。 `urlPostApplyModifier`パラメーターは、URLコマンドの後に適用されるプロトコルコマンドを指定します。このコマンドは、ユーザー指定の競合する設定を上書きします。

## 許可されたユーザーの種類 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**入力(createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | テンプレートが属する会社。 |
| `*`folderHandle`*` | `xsd:string` | はい | テンプレートが存在するフォルダーを表すフォルダーハンドル。 |
| `*`name`*` | `xsd:string` | はい | テンプレート名。 |
| `*`type`*` | `xsd:string` | はい | テンプレートタイプ。 |
| `*`urlModifier`*` | `xsd:string` | はい | ISカタログに保存され、URL上のユーザが指定したコマンドの前に適用されるImage Serverコマンドを指定します。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | URLコマンドの後に適用するプロトコルコマンドを指定します。このコマンドは、ユーザーが指定した矛盾する設定を上書きします。 |

**出力(createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | テンプレートのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコード例では、ハンドル名が`APIcreateTemplate`、`urlModifier`、および`urlPostApplyModifier`のフォルダーにテンプレートを作成します。 応答は、新しく作成されたテンプレートにハンドルを返します。

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
