---
description: トリムマージンを設定 PDFファイルで設定されるトリムマージンを設定します。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# trimMargin{#trimmargin}

トリムマージンを設定 PDFファイルで設定されるトリムマージンを設定します。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`trimMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 指定しなかった場合、 *[!DNL left]*、 *[!DNL bottom]*&#x200B;および&#x200B;*[!DNL right]*&#x200B;の値は、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
