---
description: 複数のテキストと画像レイヤーを含めることができるレイヤー画像を作成します。
solution: Experience Manager
title: createTemplate
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 10%

---


# createTemplate{#createtemplate}

複数のテキストと画像レイヤーを含めることができるレイヤー画像を作成します。

`urlModifier`パラメータは、URL上でユーザが指定したコマンドの前に適用するImage Serverカタログに保存されるImage Serverプロトコルコマンドを指定します。 `urlPostApplyModifier`パラメーターは、URLコマンドの後に適用するプロトコルコマンドを指定します。これにより、ユーザーが入力した設定の競合が上書きされます。

## 認証済みユーザータイプ{#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | テンプレートが属する会社。 |
| `*`folderHandle`*` | `xsd:string` | はい | テンプレートが存在するフォルダーを表すフォルダーハンドルです。 |
| `*`name`*` | `xsd:string` | はい | テンプレート名。 |
| `*`type`*` | `xsd:string` | はい | テンプレートの種類。 |
| `*`urlModifier`*` | `xsd:string` | はい | URLでユーザが指定したコマンドの前に適用する、ISカタログに格納されたImage Serverコマンドを指定します。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | URLコマンドの後に適用するプロトコルコマンドを指定します。ユーザーが入力した設定に矛盾がある場合は、このコマンドによって上書きされます。 |

**出力(createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | テンプレートのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコードのサンプルを使用すると、ハンドル名`APIcreateTemplate`、`urlModifier`、および`urlPostApplyModifier`を持つ、指定されたフォルダーにテンプレートを作成できます。 応答は、新しく作成されたテンプレートにハンドルを返します。

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

