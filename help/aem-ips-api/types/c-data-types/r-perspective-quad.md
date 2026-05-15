---
description: getPhotoshopPath操作によって返される画像の位置座標。
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
TQID: 'https://experienceleague.adobe.com/jJYhv5-HhU2t1CyVeRVzmIsprZ3xM4ZQtcMDS-Zgt6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 6%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath操作によって返される画像の位置座標。

構文

## パラメーター {#section-59792c446366456d90de7f5875bad1b0}

| 名前 | 種類 | 説明 |
|---|---|---|
| x0 | `xsd:double` | 左上のx軸座標。 |
| y0 | `xsd:double` | 左上のY軸座標。 |
| x1 | `xsd:double` | 右上のx軸座標。 |
| y1 | `xsd:double` | 右上のY軸座標。 |
| x2 | `xsd:double` | 右下のx軸座標。 |
| y2 | `xsd:double` | 右下のY軸座標。 |
| x3 | `xsd:double` | 左下のX軸の座標。 |
| y3 | `xsd:double` | 左下のY軸座標。 |

## 例 {#section-19ed4409ff3a41c9b52a9c9424612927}

`PerspectiveQuad` タイプは、次の順序でデータを返します。

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)
