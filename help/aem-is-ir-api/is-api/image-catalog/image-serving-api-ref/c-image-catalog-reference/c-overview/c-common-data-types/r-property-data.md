---
description: プロパティデータは、1 つ以上のプロパティを表すテキスト文字列で構成されます。
solution: Experience Manager
title: プロパティデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# プロパティデータ{#property-data}

プロパティデータは、1 つ以上のプロパティを表すテキスト文字列で構成されます。

プロパティは、プロパティ名とプロパティ値で構成され、=で区切られます。

複数のプロパティは行区切りで区切られ、`??` または `<CR><LF>` のいずれかになります。 プロパティ データ文字列全体が引用符で囲まれていない場合、サーバはデータをクライアントに送信する前に、`??` の各出現箇所を `<CR><LF>` に置き換えます。 プロパティ名には、文字、数字、「。」、「–」、「_」を使用できます。 プロパティ名では、大文字と小文字が区別されません。

プロパティ値に行区切り記号を含めることはできません。

プロパティデータに適用されるその他のルールについては、[ テキスト文字列 ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) を参照してください。
