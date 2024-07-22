---
description: メディアの余白を設定します。 PDFファイルに設定されているメディアの余白を設定します。
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

メディアの余白を設定します。 PDFファイルに設定されているメディアの余白を設定します。

ポイント ` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`

デフォルトでは、`mediaMargin` は `viewWidth` および `viewHeight` で定義されたドキュメントのフルサイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、*[!DNL right]* の値は、指定されていない場合、デフォルトで *[!DNL top]* の値に設定されます。
