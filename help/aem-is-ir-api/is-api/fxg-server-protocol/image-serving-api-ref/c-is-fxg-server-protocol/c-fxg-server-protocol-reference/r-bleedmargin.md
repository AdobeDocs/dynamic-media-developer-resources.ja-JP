---
description: 裁ち落としマージンを設定 PDFファイルで設定される裁ち落としマージンを設定します。
solution: Experience Manager
title: 薄い
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# bleedmargin{#bleedmargin}

裁ち落としマージンを設定 PDFファイルで設定される裁ち落としマージンを設定します。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`bleedMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、および&#x200B;*[!DNL right]*&#x200B;の値が指定されない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
