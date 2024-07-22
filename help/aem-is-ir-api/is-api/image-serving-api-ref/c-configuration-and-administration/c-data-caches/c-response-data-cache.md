---
title: 応答データキャッシュ
description: は  [!DNL Platform Server]  リクエストがキャッシュ不可とマークされていない限り、すべての返信画像と特定のテキストデータをディスクにキャッシュします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 応答データキャッシュ{#response-data-cache}

リク [!DNL Platform Server] ストがキャッシュ不可とマークされていない限り、すべての返信画像と特定のテキストデータがキャッシュされます。

[!DNL Platform Server] のディスクキャッシュの場所は `PS::cache.rootPaths` で設定されます。

キャッシュヒット率が高いアプリケーションの場合は、複数のディスクデバイスに応答データキャッシュを分散させることで、サーバーのパフォーマンスと容量を増やすことができます。 これを行うには、各ディスクにキャッシュルートフォルダーを作成し、`PS::cache.rootPaths` に登録します。

`PS::cache.maxSize` は、ファイルシステムのオーバーヘッドを考慮せずに、すべてのキャッシュエントリの合計サイズを指定します。 必要なディスク容量は、ディスク・ブロック・サイズやキャッシュ・エントリの数など、ファイル・システムのプロパティによって異なります。 HTTP ディスクキャッシュ用に、`PS::cache.maxSize` で指定された量の 2 倍のディスク領域を予約します。 キャッシュされたデータの量を制限の範囲内に保つために、最も新しく使用されていないアルゴリズムが使用されます。

`PS::cache.maxSize` に加えて、応答キャッシュも、`PS::cache.maxEntries` でキャッシュエントリの最大数を制限することで管理されます。 Linux® では、この設定は、キャッシュパーティションで使用可能な inode の数以下の値を指定する必要があります。

>[!NOTE]
>
>[!DNL Platform Server] は、メモリ内キャッシュインデックスを維持します。 このインデックスのサイズは、`PS::cache.maxEntries` の値の 32 バイト倍です。 必要に応じて、大きなキャッシュに対応するように [!DNL Platform Server] ヒープサイズを増やします。

システムは、サーバーが正常にシャットダウンされたときにディスクに保存されるキャッシュインデックスファイルを使用します。 電源障害などの予期しないイベントが発生した場合、このファイルは保存されない可能性があります。 また、[!DNL Platform Server] が準備できるまでに数分かかる場合があります。
