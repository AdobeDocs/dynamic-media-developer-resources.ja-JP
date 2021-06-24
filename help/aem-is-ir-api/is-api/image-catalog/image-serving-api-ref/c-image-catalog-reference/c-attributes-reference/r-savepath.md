---
description: saveToFile=のルートパス req=saveToFileで生成される画像の書き込み先となるルートフォルダーの相対パス。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SavePath{#savepath}

saveToFile=のルートパス req=saveToFileで生成される画像の書き込み先となるルートフォルダーの相対パス。

`SavePath` はテキスト文字列値です。

## プロパティ {#section-343d1371e966491c92854a8df14c3c50}

テキスト文字列。 空または有効な相対フォルダーパスを指定する必要があります。 常に`ImageServer::SaveDirectory`で設定された絶対ルートパスと組み合わせます。

## 初期設定 {#section-ae751eea97654f399c6aaee3f3252cbb}

定義されていない場合は`default::SavePath`から継承されます。 解決された値が空の場合、ファイルへの保存は無効になります。

## 関連項目 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
