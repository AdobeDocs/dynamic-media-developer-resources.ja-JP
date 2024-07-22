---
title: AssetSummary
description: アセットに関する要約情報を含んだメタデータ検索結果。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 9%

---

# [!DNL AssetSummary]{#assetsummary}

アセットに関する要約情報を含んだメタデータ検索結果。

構文

## パラメーター {#section-ebc75cc024d94c439260d2e71873cc74}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | アセットハンドル。 |
| タイプ | `xsd:string` | アセットタイプ。 「アセットタイプ」定数は、可能な値を定義します。 オプション。 |
| name | `xsd:string` | アセット名。 オプション。 |
| フォルダ | `xsd:string` | アセットを含むフォルダー。 |
| ファイル名 | `xsd:string` | アセットのファイル名。 |
| 作成 | `xsd:dateTime` | アセットの作成日。 |
| createUser | `xsd:string` | アセットを作成したユーザー |
| lastModified | `xsd:dateTime` | アセットが最後に更新された日付。 |
| lastModifyUser | `xsd:string` | 最後にアセットを変更したユーザー。 |
| metadataArray | `types:MetadataArray` | アセットに関連付けられたメタデータ値の配列。 |
| スコア | `xsd:double` | 類似性検索がある場合の精度を定義します（0 =一致なし、1 =完全一致）。 |
| scoreDetail | `xsd:string` | 類似性検索の結果として、類似領域に関する詳細な情報を保持します。 |
