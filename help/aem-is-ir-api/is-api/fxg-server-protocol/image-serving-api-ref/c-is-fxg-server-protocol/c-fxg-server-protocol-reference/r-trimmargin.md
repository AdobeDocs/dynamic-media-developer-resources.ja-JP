---
description: トリミングマージンを設定 PDFファイルで設定されるトリミングマージンを設定します。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# trimMargin{#trimmargin}

トリミングマージンを設定 PDFファイルで設定されるトリミングマージンを設定します。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`trimMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、および&#x200B;*[!DNL right]*&#x200B;の値が指定されない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
