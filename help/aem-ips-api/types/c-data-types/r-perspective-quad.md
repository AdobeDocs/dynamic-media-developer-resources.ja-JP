---
description: getPhotoshopPath操作で返される画像の位置の座標。
seo-description: getPhotoshopPath操作で返される画像の位置の座標。
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 15%

---


# PerspectiveQuad{#perspectivequad}

getPhotoshopPath操作で返される画像の位置の座標。

構文

## パラメータ {#section-59792c446366456d90de7f5875bad1b0}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`x0`*` | `xsd:double` | 左上のx軸の座標。 |
| `*`y0`*` | `xsd:double` | 左上のy軸の座標。 |
| `*`x1`*` | `xsd:double` | 右上のX軸座標。 |
| `*`y1`*` | `xsd:double` | 右上のy軸の座標。 |
| `*`x2`*` | `xsd:double` | 右下のX軸座標。 |
| `*`y2`*` | `xsd:double` | 右下のY軸の座標。 |
| `*`x3`*` | `xsd:double` | 左下x軸座標。 |
| `*`y3`*` | `xsd:double` | 左下のy軸の座標。 |

## 例 {#section-19ed4409ff3a41c9b52a9c9424612927}

`PerspectiveQuad`型は次の順序でデータを返します。

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

