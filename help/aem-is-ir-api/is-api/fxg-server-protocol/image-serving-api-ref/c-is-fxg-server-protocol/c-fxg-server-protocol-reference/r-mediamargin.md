---
description: メディアのマージンを設定 PDFファイルに設定されたメディアマージンを設定します。
solution: Experience Manager
title: mediaMargin
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# mediaMargin{#mediamargin}

メディアのマージンを設定 PDFファイルに設定されたメディアマージンを設定します。

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`mediaMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、および&#x200B;*[!DNL right]*&#x200B;の値が指定されない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
