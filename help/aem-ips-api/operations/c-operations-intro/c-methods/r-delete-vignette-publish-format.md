---
description: ビネット公開形式を削除します。
solution: Experience Manager
title: deleteVignetPublishFormat
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 13%

---


# deleteVignetPublishFormat{#deletevignettepublishformat}

ビネット公開形式を削除します。

## 認証済みユーザータイプ{#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-789625ba29df4b5f880914d4c64f77ce}

**入力(deleteVignettePublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | ビネットが属する会社のハンドル。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | はい | 削除するビネット公開形式のハンドル。 |

**出力(deleteVignettePublishFormatParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

次のコードサンプルを使用すると、ハンドルで指定されたビネット公開形式を削除できます。

**リクエスト**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**応答**

なし
