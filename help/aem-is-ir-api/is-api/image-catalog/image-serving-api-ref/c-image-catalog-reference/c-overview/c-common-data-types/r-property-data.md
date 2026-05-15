---
description: プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。
solution: Experience Manager
title: プロパティデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# プロパティデータ{#property-data}

プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。

プロパティは、プロパティ名とプロパティ値で構成され、=で区切られます。

複数のプロパティは、行の区切り記号（`??`または`<CR><LF>`）で区切られます。 プロパティ データ文字列全体が引用符で囲まれていない場合、データをクライアントに送信する前に、サーバーは`??`の各出現を`<CR><LF>`に置き換えます。 プロパティ名には、文字、数字、「。」、「 – 」、「_」を使用できます。 プロパティ名では、大文字と小文字は区別されません。

プロパティの値に行区切り記号を含めることはできません。

プロパティデータに適用される追加のルールについては、[ テキスト文字列](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)を参照してください。
