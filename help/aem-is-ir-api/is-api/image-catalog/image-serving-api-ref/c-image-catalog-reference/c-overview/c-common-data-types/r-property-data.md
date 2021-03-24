---
description: プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。
solution: Experience Manager
title: プロパティデータ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# プロパティデータ{#property-data}

プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。

プロパティは、プロパティ名とプロパティ値で構成され、それぞれ=で区切られます。

複数のプロパティは、`??`または`<CR><LF>`のいずれかの行区切り文字で区切られます。 プロパティデータ文字列全体が引用符で囲まれていない場合、サーバーはデータをクライアントに送信する前に、`??`の各オカレンスを`<CR><LF>`で置き換えます。 プロパティ名は、英数字、「。」、「 — 」および「_」で構成できます。 プロパティ名では大文字と小文字は区別されません。

プロパティ値に行区切り文字を含めることはできません。

プロパティデータに適用される追加のルールについては、「[テキスト文字列](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)」を参照してください。
