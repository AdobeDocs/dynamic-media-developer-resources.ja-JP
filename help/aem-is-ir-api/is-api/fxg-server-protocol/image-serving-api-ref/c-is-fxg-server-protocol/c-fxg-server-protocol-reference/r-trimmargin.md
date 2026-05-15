---
description: トリムマージンを設定します。 PDF ファイルに設定されているトリムマージンを設定します。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
TQID: 'https://experienceleague.adobe.com/xrj1Qk8XDpN0r45H5uB2rkq6cq2xP8sn5LobTtKtxG4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# trimMargin{#trimmargin}

トリムマージンを設定します。 PDF ファイルに設定されているトリムマージンを設定します。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` ポイント

デフォルトでは、`trimMargin`は`viewWidth`と`viewHeight`によって定義されたドキュメントのフルサイズに設定されています。 *[!DNL left]*、*[!DNL bottom]*&#x200B;および&#x200B;*[!DNL right]*&#x200B;の値は、指定されていない場合、デフォルトで&#x200B;*[!DNL top]*&#x200B;値になります。
