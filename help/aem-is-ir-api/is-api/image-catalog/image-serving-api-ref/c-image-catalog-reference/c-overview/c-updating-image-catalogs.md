---
description: サーバは、カタログフォルダを継続的に監視し、メインのカタログ属性ファイルが変更されたことを検出すると、関連するカタログデータファイルを含む画像カタログを自動的に再読み込みします。
solution: Experience Manager
title: 画像カタログの更新
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 画像カタログの更新{#updating-image-catalogs}

サーバは、カタログフォルダを継続的に監視し、メインのカタログ属性ファイルが変更されたことを検出すると、関連するカタログデータファイルを含む画像カタログを自動的に再読み込みします。

サーバー上の画像カタログを更新するには、まず変更が必要なすべてのカタログデータファイルを置き換えてから、カタログの再読み込みをトリガーするカタログ属性ファイルを置き換えます（「タッチ」してファイルの日付を更新します）。

## 増分更新 {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

大きな画像カタログの読み込みと処理は、サーバーに大きな負荷をかける可能性があり、ライブサービング操作に悪影響を及ぼす可能性があります。 この影響を最小限に抑えるには、次のように機能する増分カタログ更新メカニズムを実装することをお勧めします。

すべての画像を含むプライマリカタログファイルは、低トラフィック時間中に夜間に読み込まれます。 画像カタログ内のレコードを追加または変更する必要がある場合は、新しいレコードまたは変更されたレコードのみを含む別の画像データファイルが作成されます。 このファイルは、`attribute::CatalogFile`にセカンダリイメージデータファイルとして登録されます。 サーバーは、カタログ属性ファイルが変更されたことを検出し、変更されたカタログデータファイルを確認します。 メイン画像データファイルに何も操作されていない場合、サーバーは増分データファイルのみを読み込むか、リロードします。 このファイルは通常、メインカタログファイルよりもはるかに小さいので、メインカタログを再読み込みする場合と比べて、サーバーへの影響は大幅に軽減されます。

増分更新をおこなうと、トラフィックが多い場合にサーバーに与える影響が大幅に軽減されます。 最適なサーバーパフォーマンスを維持するために、低トラフィック時間帯に、増分カタログデータファイルをメインカタログデータファイルに定期的に結合することをお勧めします。
