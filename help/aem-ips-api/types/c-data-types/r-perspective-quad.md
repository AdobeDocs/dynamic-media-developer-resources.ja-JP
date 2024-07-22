---
description: getPhotoshopPath 操作によって返される画像の場所の座標。
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath 操作によって返される画像の場所の座標。

構文

## パラメーター {#section-59792c446366456d90de7f5875bad1b0}

| 名前 | 種類 | 説明 |
|---|---|---|
| x0 | `xsd:double` | 左上の x 軸座標。 |
| y0 | `xsd:double` | 左上の Y 軸座標。 |
| x1 | `xsd:double` | 右上の x 軸座標。 |
| y1 | `xsd:double` | 右上の Y 軸座標。 |
| x2 | `xsd:double` | 右下の X 軸座標。 |
| y2 | `xsd:double` | 右下の Y 軸座標。 |
| x3 | `xsd:double` | 左下の X 軸の座標。 |
| y3 | `xsd:double` | 左下の Y 軸座標。 |

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
