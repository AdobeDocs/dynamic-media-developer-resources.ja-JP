---
description: トリミングマージンを設定 PDFファイルで設定されるトリミングマージンを設定します。
seo-description: トリミングマージンを設定 PDFファイルで設定されるトリミングマージンを設定します。
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# trimMargin{#trimmargin}

トリミングマージンを設定 PDFファイルで設定されるトリミングマージンを設定します。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`trimMargin`は`viewWidth`と`viewHeight`で定義されているドキュメントの最大サイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、および&#x200B;*[!DNL right]*&#x200B;の値が指定されない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値に設定されます。
