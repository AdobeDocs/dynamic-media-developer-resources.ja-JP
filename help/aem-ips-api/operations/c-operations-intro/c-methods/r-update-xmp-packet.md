---
description: アセットのXMPメタデータパケットを設定または更新します。
solution: Experience Manager
title: updateXMPPacket
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 04d85dba-cc86-4069-ab5d-9a5b3fe542c9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 24%

---

# updateXMPPacket{#updatexmppacket}

アセットのXMPメタデータパケットを設定または更新します。

構文

## 許可されたユーザーの種類 {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalcontribUser`

## パラメータ {#section-7a89621d441840faba639746b410a489}

**入力(updateXMPPacketParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| `*`compressedPacket`*` | `xsd:Base 64 binary` | はい | [!DNL zlib-compressed] 設定または更新するXMPパケット。 |

**出力(updateXMPPacketReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`成功`*` | `xsd:boolean` | はい | パケットが更新された場合は`true`を返します。 |

## 例 {#section-38b556b94e5044bf97a954519ff6c212}

**リクエスト**

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**応答**

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```
