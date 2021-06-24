---
description: プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。
solution: Experience Manager
title: プロパティデータ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# プロパティデータ{#property-data}

プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。

プロパティは、プロパティ名とプロパティ値で構成され、=で区切られます。

複数のプロパティは、行区切りで区切ります。`??`または`<CR><LF>`を指定できます。 プロパティデータ文字列全体を引用符で囲まない場合、サーバーは、`??`のそれぞれを`<CR><LF>`に置き換えてから、クライアントにデータを送信します。 プロパティ名は、英数字、「。」、「 — 」、「_」で構成することができます。 プロパティ名では大文字と小文字が区別されません。

プロパティ値に行の区切り文字を含めることはできません。

プロパティデータに適用される追加のルールについては、「[テキスト文字列](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)」を参照してください。
