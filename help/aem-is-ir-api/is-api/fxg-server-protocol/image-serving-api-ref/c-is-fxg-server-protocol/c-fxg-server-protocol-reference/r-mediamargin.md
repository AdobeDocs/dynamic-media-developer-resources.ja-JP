---
description: メディアの余白を設定します。 PDFファイルに設定されたメディアの余白を設定します。
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

メディアの余白を設定します。 PDFファイルに設定されたメディアの余白を設定します。

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`mediaMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 指定しなかった場合、 *[!DNL left]*、 *[!DNL bottom]*&#x200B;および&#x200B;*[!DNL right]*&#x200B;の値は、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
