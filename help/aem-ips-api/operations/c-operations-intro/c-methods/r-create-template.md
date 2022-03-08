---
description: 複数のテキストと画像のレイヤーを持つことができるレイヤー画像を作成します。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# createTemplate{#createtemplate}

複数のテキストと画像のレイヤーを持つことができるレイヤー画像を作成します。

この `urlModifier` パラメータは、URL 上でユーザが指定したコマンドの前に適用される Image Server カタログに保存される Image Server プロトコルコマンドを指定します。 この `urlPostApplyModifier` パラメータは、URL コマンドの後に適用されるプロトコルコマンドを指定します。このコマンドは、ユーザが指定した設定の競合を無効にします。

## 認証済みユーザータイプ {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**入力 (createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | テンプレートが属する会社。 |
| folderHandle | `xsd:string` | はい | テンプレートが存在するフォルダーを表すフォルダーハンドル。 |
| name | `xsd:string` | はい | テンプレート名。 |
| タイプ | `xsd:string` | はい | テンプレートタイプ。 |
| urlModifier | `xsd:string` | はい | IS カタログに保存され、URL 上のユーザが指定したコマンドの前に適用される Image Server コマンドを指定します。 |
| urlPostApplyModifier | `xsd:string` | いいえ | URL コマンドの後に適用するプロトコルコマンドを指定します。このコマンドは、ユーザが指定した設定の競合を無効にします。 |

**出力 (createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | テンプレートのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコード例では、ハンドルで指定されたフォルダーに、という名前のテンプレートを作成します。 `APIcreateTemplate`, a `urlModifier`、および `urlPostApplyModifier`. 応答は、新しく作成されたテンプレートにハンドルを返します。

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
