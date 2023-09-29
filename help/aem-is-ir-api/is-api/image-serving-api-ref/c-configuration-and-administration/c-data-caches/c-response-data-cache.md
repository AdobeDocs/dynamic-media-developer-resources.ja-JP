---
title: 応答データキャッシュ
description: The [!DNL Platform Server] 要求が非キャッシュ可能とマークされていない限り、すべての返信画像と特定のテキストデータをディスクにキャッシュします。
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

The [!DNL Platform Server] 要求がキャッシュ不可とマークされていない場合を除き、すべての返信画像と特定のテキストデータをディスクにキャッシュします。

の場所 [!DNL Platform Server]のディスクキャッシュは次を使用して設定されています： `PS::cache.rootPaths`.

キャッシュヒット率の高いアプリケーションの場合は、応答データのキャッシュを複数のディスクデバイスに分散することで、サーバのパフォーマンスと容量を向上させることができます。 これを実現するには、各ディスクにキャッシュルートフォルダーを作成し、それらをに登録します。 `PS::cache.rootPaths`.

The `PS::cache.maxSize` すべてのキャッシュエントリの合計サイズを指定します。ファイルシステムのオーバーヘッドは考慮されません。 必要なディスク容量は、ディスクブロックサイズやキャッシュエントリの数など、ファイルシステムのプロパティによって異なります。 HTTP ディスクキャッシュ用のディスク領域を、 `PS::cache.maxSize`. キャッシュされたデータの量を制限内に保つために、最近使用されなかったアルゴリズムが使用されます。

に加えて `PS::cache.maxSize`に設定する場合、応答キャッシュは、 `PS::cache.maxEntries`. Linux®では、この設定はキャッシュパーティション上の使用可能な inode の数以下の値を指定する必要があります。

>[!NOTE]
>
>The [!DNL Platform Server] はメモリ内キャッシュインデックスを維持します。 このインデックスのサイズは、 `PS::cache.maxEntries`. を増やす [!DNL Platform Server] 必要に応じて、より大きなキャッシュに対応するヒープサイズ。

システムは、サーバが正常にシャットダウンされたときにディスクに保存されるキャッシュインデックスファイルを使用します。 電源障害などの予期しないイベントが発生した場合は、このファイルが保存されない可能性があります。 また、 [!DNL Platform Server] 準備が整う
