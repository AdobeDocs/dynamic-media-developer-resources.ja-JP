---
title: pscan
description: プログレッシブJPEGスキャン。 プログレッシブJPEGでは、最初は全体がぼやけて低画質の写真が表示されるように、画像が表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
TQID: 'https://experienceleague.adobe.com/NhxrMkCLJuVcoakGVk7akMWm6Po9a-CSSegTqHLXMbo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 2%

---

# pscan{#pscan}

プログレッシブJPEGスキャン。 プログレッシブJPEGでは、最初は全体がぼやけて低画質の写真が表示されるように、画像が表示されます。 スキャンが続くと、画像のデータがより完全にダウンロードされるにつれて、より明確になります。 このパラメーターを使用すると、画像全体が表示されるまでのスキャン回数（3、4、または5）を設定できます。

`pscan=auto|3|4|5`

各スキャンの実際の速度は、ユーザーのシステムとデータを受信して解凍するコンピューターの送信速度によって異なります。

`Auto`は、独立したJPEG ライブラリによって計算され、カラーモデルに依存するスキャン設定を使用します。 `3`、`4`、`5`の値は、JPEG ファイルをpjpeg （プログレッシブ JPEG）として保存する際にAdobe Photoshopで見つかったスキャン設定に対応しています。

`pscan`が設定されていない場合、デフォルトは`auto`になります。

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 出力フォーマットがプログレッシブ JPEGでない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
