---
description: アセットに関する要約された情報を含むメタデータ検索結果。
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 11%

---


# AssetSummary{#assetsummary}

アセットに関する要約された情報を含むメタデータ検索結果。

構文

## パラメータ {#section-ebc75cc024d94c439260d2e71873cc74}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | アセットハンドル |
| `*`type`*` | `xsd:string` | アセットタイプ. 使用可能な値は、&quot;Asset Types&quot;定数で定義します。 （オプション） |
| `*`name`*` | `xsd:string` | アセット名。 （オプション） |
| `*`フォルダ`*` | `xsd:string` | アセットを含むフォルダーです。 |
| `*`ファイル名`*` | `xsd:string` | アセットのファイル名。 |
| `*`作成`*` | `xsd:dateTime` | アセット作成日。 |
| `*`createUser`*` | `xsd:string` | アセットを作成したユーザー。 |
| `*`lastModified`*` | `xsd:dateTime` | アセットが最後に更新された日付。 |
| `*`lastModifyUser`*` | `xsd:string` | アセットを最後に変更したユーザー。 |
| `*`metadataArray`*` | `types:MetadataArray` | アセットに関連付けられているメタデータ値の配列。 |
| `*`スコア`*` | `xsd:double` | 類似性検索の場合の精度を定義します（0 =一致なし、1 =完全一致）。 |
| `*`scoreDetail`*` | `xsd:string` | 類似性検索の結果として、類似する領域に関する詳細情報が保持されます。 |

