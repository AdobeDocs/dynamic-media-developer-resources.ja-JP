---
description: 裁ち落とし余白を設定します。 PDFファイルに設定されている裁ち落とし余白を設定します。
solution: Experience Manager
title: 裁ち余白
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# 裁ち余白{#bleedmargin}

裁ち落とし余白を設定します。 PDFファイルに設定されている裁ち落とし余白を設定します。

ポイント `bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`

デフォルトでは、`bleedMargin` は `viewWidth` および `viewHeight` で定義されたドキュメントのフルサイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、*[!DNL right]* の値は、指定されていない場合、デフォルトで *[!DNL top]* の値に設定されます。
