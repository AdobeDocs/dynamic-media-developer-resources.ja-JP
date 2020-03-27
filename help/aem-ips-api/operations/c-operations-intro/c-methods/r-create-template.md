---
description: 複数のテキストおよび画像レイヤーを含むことができるレイヤー画像を作成します。
seo-description: 複数のテキストおよび画像レイヤーを含むことができるレイヤー画像を作成します。
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createTemplate{#createtemplate}

複数のテキストおよび画像レイヤーを含むことができるレイヤー画像を作成します。

このパラ `urlModifier` メータは、URL上でユーザが指定したコマンドの前に適用されるImage Serverカタログに格納されるImage Serverプロトコルコマンドを指定します。 このパラメ `urlPostApplyModifier` ーターは、URLコマンドの後に適用されるプロトコルコマンドを指定します。このコマンドは、ユーザーが指定した設定の競合を上書きします。

## 認証されたユーザータイプ {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | テンプレートが属する会社。 |
| ` *`folderHandle`*` | `xsd:string` | はい | テンプレートが存在するフォルダーを表すフォルダーハンドルです。 |
| ` *`name`*` | `xsd:string` | はい | テンプレート名。 |
| ` *`type`*` | `xsd:string` | はい | テンプレートタイプ。 |
| ` *`urlModifier`*` | `xsd:string` | はい | URL上でユーザが指定したコマンドの前に適用される、ISカタログに保存されたImage Serverコマンドを指定します。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | いいえ | URLコマンドの後に適用するプロトコルコマンドを指定します。このコマンドは、ユーザーが指定した設定の競合を上書きします。 |

**出力(createTemplateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | はい | テンプレートのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコード例では、ハンドルで指定されたフォルダーに、名前が、、、およびのテンプ `APIcreateTemplate`レートを作 `urlModifier`成していま `urlPostApplyModifier`す。 応答は、新しく作成されたテンプレートにハンドルを返します。

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

