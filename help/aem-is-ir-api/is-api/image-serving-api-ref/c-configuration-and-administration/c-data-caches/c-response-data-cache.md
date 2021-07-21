---
description: リクエストがキャッシュ不可とマークされていない限り、Platform Serverはすべての返信画像と特定のテキストデータをディスクにキャッシュします。
solution: Experience Manager
title: 応答データキャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 応答データキャッシュ{#response-data-cache}

リクエストがキャッシュ不可とマークされていない限り、Platform Serverはすべての返信画像と特定のテキストデータをディスクにキャッシュします。

Platform Serverのディスクキャッシュの場所は`PS::cache.rootPaths`で設定されます。

キャッシュヒット率の高いアプリケーションでは、複数のディスクデバイスにレスポンスデータキャッシュを配布することで、サーバのパフォーマンスと容量を向上できます。 これを実現するには、各ディスクにキャッシュルートフォルダを作成し、`PS::cache.rootPaths`に登録します。

`PS::cache.maxSize` すべてのキャッシュ・エントリの合計サイズを指定します。ファイル・システムのオーバーヘッドは考慮されません。実際に必要なディスク領域の量は、ファイルシステムのプロパティ（ディスクブロックサイズやキャッシュエントリの数など）によって異なります。 `PS::cache.maxSize`で指定されている容量の2倍のディスク領域をHTTPディスクキャッシュ用に予約することをお勧めします。 キャッシュされたデータ量を制限内に保つために、最も最近使用されないアルゴリズムが使用されます。

`PS::cache.maxSize`に加えて、応答キャッシュも`PS::cache.maxEntries`で最大キャッシュエントリ数を制限することで管理されます。 Linuxでは、この設定はキャッシュパーティションで使用可能なinodeの数以下の値を指定する必要があります。

>[!NOTE]
>
>Platform Serverは、メモリ内キャッシュインデックスを維持します。 このインデックスのサイズは`PS::cache.maxEntries`の値の32バイトです。 より大きなキャッシュに対応するために、Platform Serverのヒープサイズを増やす必要が生じる場合があります。

システムは、サーバが正常にシャットダウンされたときにディスクに保存されるキャッシュインデックスファイルを使用します。 電源障害などの予期しないイベントが発生した場合、このファイルは保存されない可能性があります。 また、Platform Serverが準備されるまで数分かかる場合があります。
