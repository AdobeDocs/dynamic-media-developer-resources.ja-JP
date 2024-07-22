---
description: 複数のテキストと画像レイヤーを持つレイヤー化された画像を作成します。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 9%

---

# createTemplate{#createtemplate}

複数のテキストと画像レイヤーを持つレイヤー化された画像を作成します。

`urlModifier` パラメーターは、URL でユーザー指定のコマンドの前に適用される、Image Server カタログに保存されている Image Server プロトコルコマンドを指定します。 `urlPostApplyModifier` パラメーターは、競合するユーザー指定の設定を上書きする URL コマンドの後に適用されるプロトコル コマンドを指定します。

## 許可されているユーザータイプ {#section-9fb615d8e75f452eab2893cc3decfbe6}

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
| folderHandle | `xsd:string` | はい | テンプレートが存在するフォルダーを表すフォルダーハンドル。 |
| name | `xsd:string` | はい | テンプレート名。 |
| タイプ | `xsd:string` | はい | テンプレートタイプ。 |
| urlModifier | `xsd:string` | はい | URL 上でユーザー指定のコマンドの前に適用される、IS カタログに格納された Image Server コマンドを指定します。 |
| urlPostApplyModifier | `xsd:string` | いいえ | 競合するユーザー指定の設定を上書きする URL コマンドの後に適用されるプロトコル コマンドを指定します。 |

**出力（createTemplateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | テンプレートへのハンドル。 |

## 例 {#section-09adb4d2f0c944af875c4463a461f55d}

このコードサンプルでは、ハンドルで指定されたフォルダーに、名前 `APIcreateTemplate`、`urlModifier`、`urlPostApplyModifier` を使用してテンプレートを作成します。 応答は、新しく作成されたテンプレートへのハンドルを返します。

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
