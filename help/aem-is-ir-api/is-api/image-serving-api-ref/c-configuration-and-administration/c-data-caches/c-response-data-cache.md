---
title: 応答データキャッシュ
description: ' [!DNL Platform Server] は、リクエストがキャッシュ不可とマークされていない限り、すべての返信画像と特定のテキストデータをディスクにキャッシュします。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# 応答データキャッシュ{#response-data-cache}

[!DNL Platform Server]は、リクエストがキャッシュ不可としてマークされていない限り、すべての返信画像と特定のテキストデータをディスクにキャッシュします。

[!DNL Platform Server]のディスクキャッシュの場所は`PS::cache.rootPaths`に設定されています。

キャッシュヒット率が高いアプリケーションの場合、複数のディスクデバイス間で応答データキャッシュを分散することで、サーバーのパフォーマンスと容量を向上させることができます。 これを実現するには、各ディスクにキャッシュ ルート フォルダーを作成し、`PS::cache.rootPaths`に登録します。

`PS::cache.maxSize`は、ファイルシステムのオーバーヘッドを考慮せずに、すべてのキャッシュエントリの合計サイズを指定します。 必要なディスク容量は、ディスクブロックサイズなどのファイルシステムのプロパティとキャッシュエントリの数によって異なります。 HTTP ディスクキャッシュのディスク容量は、`PS::cache.maxSize`で指定された容量の2倍を確保してください。 最も最近使用されていないアルゴリズムを使用して、キャッシュされたデータ量を制限内に保ちます。

`PS::cache.maxSize`に加えて、応答キャッシュは、`PS::cache.maxEntries`でキャッシュエントリの最大数を制限することによって管理されます。 Linux®では、この設定では、キャッシュパーティションで使用可能なノード数を超えない値を指定する必要があります。

>[!NOTE]
>
>[!DNL Platform Server]はメモリ内キャッシュ インデックスを保持します。 このインデックスのサイズは、値`PS::cache.maxEntries`の32 バイト倍です。 必要に応じて、より大きなキャッシュに対応するために、[!DNL Platform Server] ヒープサイズを増やします。

システムは、サーバーが整然とシャットダウンされたときにディスクに保存されるキャッシュインデックスファイルを使用します。 電源障害などの予期しないイベントが発生した場合、このファイルは保存されない可能性があります。 また、[!DNL Platform Server]の準備が整うまでに数分かかる場合もあります。
