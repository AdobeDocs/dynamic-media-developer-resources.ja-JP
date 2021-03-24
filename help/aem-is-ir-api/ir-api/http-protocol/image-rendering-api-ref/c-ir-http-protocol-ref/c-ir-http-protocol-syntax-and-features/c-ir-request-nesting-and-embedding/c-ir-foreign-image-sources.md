---
description: 画像サービングでは、外部のHTTPサーバおよびFTPサーバ上のソース画像へのアクセスがサポートされています。
solution: Experience Manager
title: 外部画像ソース
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 外部画像ソース{#foreign-image-sources}

画像サービングでは、外部のHTTPサーバおよびFTPサーバ上のソース画像へのアクセスがサポートされています。

`src=`または`mask=`コマンドの外部URLを指定するには；埋め込まれたURL全体を波括弧で囲みます。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対URL（`attribute::AllowDirectUrls`が設定されている場合）および`attribute::RootUrl`を基準としたURLを使用できます。 絶対URLが埋め込まれ、属性が次の場合にエラーが発生します。`AllowDirectUrls`が0の場合、または相対URLが指定され、`attribute::RootUrl`が空の場合。

外部イメージは、HTTP応答に含まれるキャッシュヘッダーに従ってサーバーによってキャッシュされます。
