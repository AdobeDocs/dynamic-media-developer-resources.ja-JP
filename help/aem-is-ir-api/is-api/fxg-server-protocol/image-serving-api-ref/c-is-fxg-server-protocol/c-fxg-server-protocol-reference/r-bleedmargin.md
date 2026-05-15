---
description: 裁ち落としのマージンを設定 PDF ファイルに設定されている裁ち落としマージンを設定します。
solution: Experience Manager
title: 裁ち落とし
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
TQID: 'https://experienceleague.adobe.com/Lghb-4jpksjewoUjBD-SE9UqsD6AX6WFwb2sbkCobXE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# 裁ち落とし{#bleedmargin}

裁ち落としのマージンを設定 PDF ファイルに設定されている裁ち落としマージンを設定します。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`bleedMargin`は`viewWidth`と`viewHeight`によって定義されたドキュメントのフルサイズに設定されています。 *[!DNL left]*、*[!DNL bottom]*&#x200B;および&#x200B;*[!DNL right]*&#x200B;の値は、指定されていない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値になります。
