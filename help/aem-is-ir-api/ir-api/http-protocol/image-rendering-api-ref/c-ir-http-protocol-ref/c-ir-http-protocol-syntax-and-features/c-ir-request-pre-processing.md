---
title: リクエストの事前処理
description: 画像レンダリングは、正規表現の一致ルールと置換ルールに基づくシンプルなリクエストプリプロセッサを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# リクエストの事前処理{#request-pre-processing}

画像レンダリングは、正規表現の一致ルールと置換ルールに基づくシンプルなリクエストプリプロセッサを提供します。

ルールのコレクション（ルールセット）は、デフォルトカタログを含む各マテリアルカタログに添付できます。 ルールは、XML形式のファイルで指定します。

リクエスト前処理ルールは、画像レンダリングパーサーで処理される前に、リクエストのパスとクエリ部分を変更できます。 この手順には、パスの操作、コマンドの追加、コマンド値の変更、テンプレートまたはマクロの適用が含まれます。 また、デフォルトの返信画像サイズの設定やHTTP サービスの特定のクライアント IP アドレスへの制限など、通常はカタログ属性のみで制御される特定の機能を設定および上書きするためにルールを使用することもできます。

リクエスト前処理ルールは、以下に示すような様々なアプリケーションに適しています。

* *仮想パス* メカニズムを実装します。これにより、リクエストパスをファイル、FTP、およびHTTP パスに再マッピングできます。
* サーバーの不正使用を防ぐために、CPUを多用するコマンドの使用を禁止します。
* リクエストパスや画像名に応じて、画質の設定（JPEG画質やシャープニングなど）を制御します。

ルールセットの作成、使用、管理に関する詳細は、ルールセットリファレンスを参照してください。

ルールセット参照、属性：:RuleSetFileも参照してください。

