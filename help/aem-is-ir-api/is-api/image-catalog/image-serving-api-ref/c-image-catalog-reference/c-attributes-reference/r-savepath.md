---
description: Savetofile=のルートパス。 req=saveToFile で生成された画像の書き込み先ルートフォルダーの相対パス。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# SavePath{#savepath}

Savetofile=のルートパス。 req=saveToFile で生成された画像の書き込み先ルートフォルダーの相対パス。

`SavePath` はテキスト文字列値です。

## プロパティ {#section-343d1371e966491c92854a8df14c3c50}

テキスト文字列 空または有効な相対フォルダーパスにする必要があります。 常に `ImageServer::SaveDirectory` で設定された絶対ルートパスと組み合わせます。

## 初期設定 {#section-ae751eea97654f399c6aaee3f3252cbb}

定義されていない場合は `default::SavePath` から継承します。 解決された値が空の場合、ファイルへの保存は無効になります。

## 関連項目 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
