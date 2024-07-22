---
description: ズームターゲットを削除します。
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 9%

---

# deleteZoomTarget{#deletezoomtarget}

ズームターゲットを削除します。

## 許可されているユーザータイプ {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび書き込みアクセス権が必要です。

## パラメーター {#section-225330a45e7a408f8375e084677d9cb1}

**入力（deleteZoomTargetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ズームターゲットが属する会社へのハンドル。 |
| zoom ターゲット ハンドル | `xsd:string` | はい | 削除するズームターゲットへのハンドル。 |

**出力（deleteZoomTargetParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-a35857a5ca884357a879f7ba6cf985fe}

このコードサンプルでは、会社からズームターゲットを削除します。

**リクエスト**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**応答**

なし
