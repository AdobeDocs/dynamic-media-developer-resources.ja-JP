---
description: トリミング余白を設定します。 PDF ファイルで設定されるトリミング余白を設定します。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

トリミング余白を設定します。 PDF ファイルで設定されるトリミング余白を設定します。

ポイント ` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`

デフォルトでは、`trimMargin` は `viewWidth` および `viewHeight` で定義されたドキュメントのフルサイズに設定されます。 *[!DNL left]*、*[!DNL bottom]*、*[!DNL right]* の値は、指定されていない場合、デフォルトで *[!DNL top]* の値に設定されます。
