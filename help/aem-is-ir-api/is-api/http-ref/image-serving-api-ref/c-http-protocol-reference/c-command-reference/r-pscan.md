---
title: pscan
description: プログレッシブJPEGスキャン。 プログレッシブJPEGでは、最初は全体がぼやけたり低画質になったりする画像を表示します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# pscan{#pscan}

プログレッシブJPEGスキャン。 プログレッシブJPEGでは、最初は全体がぼやけたり低画質になったりする画像を表示します。 スキャンが進むにつれて、画像のデータがより完全にダウンロードされるにつれて、より明確になります。 このパラメーターを使用すると、画像全体を表示するために実行するスキャンの回数（3、4 または 5）を設定できます。

`pscan=auto|3|4|5`

各スキャンの実際の速度は、ユーザーのシステムの伝送速度と、データを受信および解凍するコンピューターによって異なります。

`Auto` は、独立JPEGライブラリによって計算されるスキャン設定を使用し、カラーモデルに応じて異なります。 `3`、`4`、`5` の値は、JPEGファイルを pjpeg （プログレッシブJPEG）形式で保存する際のAdobe Photoshopのスキャン設定に対応しています。

`pscan` が設定されていない場合は、デフォルトで `auto` に設定されます。

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 出力JPEGがプログレッシブフォーマットでない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
