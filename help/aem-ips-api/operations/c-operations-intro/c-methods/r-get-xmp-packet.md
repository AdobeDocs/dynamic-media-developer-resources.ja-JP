---
description: 指定されたアセットのXMPメタデータパケットを取得します。
seo-description: 指定されたアセットのXMPメタデータパケットを取得します。
seo-title: getXMPPacket
solution: Experience Manager
title: getXMPPacket
topic: Dynamic Media Image Production System API
uuid: c4b40e76-a459-4036-ace2-8df202305bf9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 20%

---


# getXMPPacket{#getxmppacket}

指定されたアセットのXMPメタデータパケットを取得します。

構文

## 認証済みユーザータイプ{#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-b4075df0e4414b00b961d978d5471db9}

**入力(getXMPPacketParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 返す会社のパケットハンドル（例：`c|656`）。 |
| `*`assetHandle`*` | `xsd:string` | はい | XMPパケットを取得する必要があるアセット。 |

**出力(getXMPPacketReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`compressedPacket`*` | `xsd:Base 64 binary` | はい | [!DNL zlib-compressed] XMPパケット。 |

## 例 {#section-d681af49122e4ca9bcd04110a2e98e6f}

**リクエスト**

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**応答**

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```

