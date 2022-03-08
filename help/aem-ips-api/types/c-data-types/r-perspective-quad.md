---
description: getPhotoshopPath 操作で返される画像の位置座標。
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 19%

---

# PerspectiveQuad{#perspectivequad}

getPhotoshopPath 操作で返される画像の位置座標。

構文

## パラメータ {#section-59792c446366456d90de7f5875bad1b0}

| 名前 | 種類 | 説明 |
|---|---|---|
| x0 | `xsd:double` | 左上の X 軸の座標。 |
| y0 | `xsd:double` | 左上の Y 軸の座標。 |
| x1 | `xsd:double` | 右上の X 軸座標。 |
| y1 | `xsd:double` | 右上の Y 軸の座標。 |
| x2 | `xsd:double` | 右下の X 軸座標。 |
| y2 | `xsd:double` | 右下の Y 軸の座標。 |
| x3 | `xsd:double` | 左下の X 軸座標。 |
| y3 | `xsd:double` | 左下の Y 軸の座標。 |

## 例 {#section-19ed4409ff3a41c9b52a9c9424612927}

この `PerspectiveQuad` type は次の順序でデータを返します。

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

