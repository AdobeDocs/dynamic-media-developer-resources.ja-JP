---
description: プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。
seo-description: プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。
seo-title: プロパティデータ
solution: Experience Manager
title: プロパティデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# プロパティデータ{#property-data}

プロパティデータは、1つ以上のプロパティを表すテキスト文字列で構成されます。

プロパティは、プロパティ名とプロパティ値で構成され、=で区切られます。

複数のプロパティは、行区切り文字（または）で区切ら `??` れます `<CR><LF>`。 プロパティデータ文字列全体が引用符で囲まれていない場合、サーバーはデータをクライアントに送信する前に、 `??` の各 `<CR><LF>` オカレンスをに置き換えます。 プロパティ名は、英数字、「。」、「 — 」および「_」で構成できます。 プロパティ名では大文字と小文字が区別されません。

プロパティ値に線の区切り文字を含めることはできません。

プロパティ [データに適用されるその他のルールについては](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) 、「テキスト文字列」を参照してください。
