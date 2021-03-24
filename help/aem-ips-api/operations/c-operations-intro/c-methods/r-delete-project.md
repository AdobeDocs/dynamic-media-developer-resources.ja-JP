---
description: 会社からプロジェクトを削除します。 アセットとプロジェクト間のリンクは無効ですが、アセットはIPSから削除されません。
solution: Experience Manager
title: deleteProject
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 8%

---


# deleteProject{#deleteproject}

会社からプロジェクトを削除します。 アセットとプロジェクト間のリンクは無効ですが、アセットはIPSから削除されません。

構文

## 認証済みユーザータイプ{#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-00d1e00dd5014513a52b4e6b4f61de62}

**入力(deleteProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | はい | プロジェクトに関連付けられている会社の名前。 |
| `*`projectHandle`*` | `xsd:string` | はい | 削除するプロジェクトのハンドル。 |

**出力(deleteProjectReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-e38507f1f7ec41b9a625f47390490254}

このコードの例では、会社ハンドルとプロジェクトハンドルを、IPS Webサービスサーバーに送信されるdeleteProjectParamのフィールドとして使用し、プロジェクトを削除します。

**リクエスト**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**応答**

なし
