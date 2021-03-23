---
description: 画像サービングは、正規式の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。
seo-description: 画像サービングは、正規式の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。
seo-title: 要求の前処理中
solution: Experience Manager
title: 要求の前処理中
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---


# リクエストの前処理{#request-preprocessing}

画像サービングは、正規式の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。

ルール（ルールセット）のコレクションは、デフォルトのカタログを含む各画像カタログに添付できます。 ルールは、XML形式のファイルを使用して指定します。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがPlatform Serverのパーサーによって処理される前に、リクエストのパスとクエリの部分を変更できます。 ルールは、通常、要求の不明化、ウォーターマーキングなどのカタログ属性のみで制御されるセキュリティ機能を設定および上書きするほか、HTTPサービスを特定のクライアントIPアドレスに制限する場合にも使用できます。

リクエストの前処理ルールは、様々なアプリケーションに適しています。その一部を次に示します。

* *仮想パス*&#x200B;メカニズムを実装し、要求パスをファイル、FTP、HTTPパスに再マップできます。
* 画像名やパスでフィルタリングされる、透かしなどのセキュリティ機能を選択して適用する。
* 特定のIPアドレスからサーバにアクセスする場合、透かしなどのセキュリティ機能を省く。
* URLパスまたはクエリ文字列内の特定のパターンを示すすべての要求または要求に、`defaultImage=`などのコマンドを強制的に適用する。
* CPU使用率の高いコマンドの使用を禁止して、サーバの乱用を防ぎます。
* ソース画像を`src=`ではなくリクエストパスで指定したまま、HTTPまたはFTPサーバー上に配置することを許可します。
* 要求パスまたは画像名に応じて、画質設定（JPEG画質やシャープなど）を制御します。

ルールセットの作成、使用、管理に関する詳細は、『[ルールセットリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)』を参照してください。

## 関連項目 {#see-also}

[ルールセットの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
