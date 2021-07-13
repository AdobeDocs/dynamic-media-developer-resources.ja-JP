---
description: 裁ち落としマージンを設定 PDFファイルで設定される裁ち落としマージンを設定します。
solution: Experience Manager
title: bleedmargin
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# bleedmargin{#bleedmargin}

裁ち落としマージンを設定 PDFファイルで設定される裁ち落としマージンを設定します。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`bleedMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 指定しなかった場合、 *[!DNL left]*、 *[!DNL bottom]*&#x200B;および&#x200B;*[!DNL right]*&#x200B;の値は、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
