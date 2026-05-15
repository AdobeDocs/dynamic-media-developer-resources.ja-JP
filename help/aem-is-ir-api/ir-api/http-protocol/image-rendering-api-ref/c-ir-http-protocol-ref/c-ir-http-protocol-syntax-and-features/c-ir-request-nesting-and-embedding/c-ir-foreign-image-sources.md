---
title: 外国の画像ソース
description: Image Servingは、外部のHTTP サーバーおよびFTP サーバー上のソース画像へのアクセスをサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# 外国の画像ソース{#foreign-image-sources}

Image Servingは、外部のHTTP サーバーおよびFTP サーバー上のソース画像へのアクセスをサポートします。

`src=`または`mask=` コマンドの外部URLを指定するには、埋め込みURL全体を中括弧で区切ります。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対URL （`attribute::AllowDirectUrls`が設定されている場合）と`attribute::RootUrl`に対する相対URLは許可されています。 絶対URLが埋め込まれ、属性：`AllowDirectUrls`が0の場合、または相対URLが指定され、`attribute::RootUrl`が空の場合、エラーが発生します。

外部イメージは、HTTP応答に含まれるキャッシングヘッダーに従ってサーバーによってキャッシュされます。
