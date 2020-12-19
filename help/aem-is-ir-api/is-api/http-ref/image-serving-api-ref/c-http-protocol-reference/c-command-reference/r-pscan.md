---
description: プログレッシブJPEGスキャン。 プログレッシブJPEGでは、画像全体がぼやけた低画質の画像で表示されます。 スキャンが続くにつれて、画像のデータが完全にダウンロードされるにつれて、スキャンがより明確になります。 このパラメーターを使用すると、画像全体をスキャンする回数（3、4または5）を設定できます。
seo-description: プログレッシブJPEGスキャン。 プログレッシブJPEGでは、画像全体がぼやけた低画質の画像で表示されます。 スキャンが続くにつれて、画像のデータが完全にダウンロードされるにつれて、スキャンがより明確になります。 このパラメーターを使用すると、画像全体をスキャンする回数（3、4または5）を設定できます。
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Scene7 Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# pscan{#pscan}

プログレッシブJPEGスキャン。 プログレッシブJPEGでは、画像全体がぼやけた低画質の画像で表示されます。 スキャンが続くにつれて、画像のデータが完全にダウンロードされるにつれて、スキャンがより明確になります。 このパラメーターを使用すると、画像全体をスキャンする回数（3、4または5）を設定できます。

`pscan=auto|3|4|5`

各スキャンの実際の速度は、ユーザーのシステムの伝送速度と、データを受信および解凍するコンピューターの伝送速度に依存します。

`Auto` は、独立したJPEGライブラリによって計算され、カラーモデルに応じて異なるスキャン設定を使用します。`3`、`4`、`5`の値は、JPEGファイルをpjpeg（プログレッシブJPEG）として保存した場合にAdobe Photoshopで見つかったスキャン設定に対応します。

`pscan`が設定されていない場合は、デフォルトで`auto`に設定されます。

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求属性。 現在のレイヤー設定に関係なく適用されます。 出力形式がプログレッシブJPEGでない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
