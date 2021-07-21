---
description: アセットに関する要約された情報を含むメタデータ検索結果。
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 11%

---

# AssetSummary{#assetsummary}

アセットに関する要約された情報を含むメタデータ検索結果。

構文

## パラメータ {#section-ebc75cc024d94c439260d2e71873cc74}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | アセットハンドル。 |
| `*`type`*` | `xsd:string` | アセットタイプ. &quot;Asset Types&quot;定数は、使用可能な値を定義します。 （オプション） |
| `*`name`*` | `xsd:string` | アセット名。 （オプション） |
| `*`フォルダ`*` | `xsd:string` | アセットを格納するフォルダー。 |
| `*`ファイル名`*` | `xsd:string` | アセットのファイル名。 |
| `*`作成`*` | `xsd:dateTime` | アセットの作成日。 |
| `*`createUser`*` | `xsd:string` | アセットを作成したユーザー。 |
| `*`lastModified`*` | `xsd:dateTime` | アセットが最後に更新された日付。 |
| `*`lastModifyUser`*` | `xsd:string` | 最後にアセットを変更したユーザー。 |
| `*`metadataArray`*` | `types:MetadataArray` | アセットに関連付けられているメタデータ値の配列。 |
| `*`スコア`*` | `xsd:double` | 類似性検索の場合の精度を定義します（0 =一致なし、1 =完全一致）。 |
| `*`scoreDetail`*` | `xsd:string` | 類似性検索の結果として、類似する領域に関する詳細情報を保持します。 |
