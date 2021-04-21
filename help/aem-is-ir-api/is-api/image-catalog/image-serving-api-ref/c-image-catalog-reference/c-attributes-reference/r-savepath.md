---
description: saveToFile=のルートパス req=saveToFileで生成された画像を書き込む必要があるルートフォルダーの相対パスです。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# SavePath{#savepath}

saveToFile=のルートパス req=saveToFileで生成された画像を書き込む必要があるルートフォルダーの相対パスです。

`SavePath` はテキスト文字列値です。

## プロパティ {#section-343d1371e966491c92854a8df14c3c50}

テキスト文字列。 空または有効な相対フォルダーパスにする必要があります。 `ImageServer::SaveDirectory`で設定された絶対ルートパスと常に組み合わせます。

## 初期設定 {#section-ae751eea97654f399c6aaee3f3252cbb}

定義されていない場合は`default::SavePath`から継承されます。 解決された値が空の場合、ファイルへの保存は無効になります。

## 関連項目 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
