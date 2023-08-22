---
title: pscan
description: プログレッシブJPEGスキャン。 プログレッシブJPEGは、最初にぼやけた低画質の写真全体を表示するように画像を表示します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# pscan{#pscan}

プログレッシブJPEGスキャン。 プログレッシブJPEGは、最初にぼやけた低画質の写真全体を表示するように画像を表示します。 スキャンが続くと、画像のデータがより完全にダウンロードされるにつれて、より明確になります。 このパラメーターを使用すると、画像全体を表示するために必要なスキャンの数 (3、4、5) を設定できます。

`pscan=auto|3|4|5`

各スキャンの実際の速度は、ユーザのシステムの伝送速度と、データを受信して解凍するコンピュータの伝送速度に依存します。

`Auto` は、独立したJPEGライブラリで計算され、カラーモデルに依存するスキャン設定を使用します。 の値 `3`, `4`, `5` は、JPEGファイルを pjpeg( プログレッシブJPEG) として保存した場合のAdobe Photoshopのスキャン設定に対応します。

次の場合 `pscan` が設定されていない場合、デフォルトはです。 `auto`.

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求属性。 現在の画層設定に関係なく適用されます。 出力形式がプログレッシブJPEGでない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
