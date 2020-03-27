---
description: 画像サービングは、正規表現の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。
seo-description: 画像サービングは、正規表現の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。
seo-title: 要求の前処理
solution: Experience Manager
title: 要求の前処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 要求の前処理{#request-preprocessing}

画像サービングは、正規表現の一致と置換ルールに基づく単純な要求プリプロセッサを提供します。

ルールのコレクション（ルールセット）は、デフォルトのカタログを含む各画像カタログに添付できます。 ルールは、XML形式のファイルで指定します。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがPlatform Serverのパーサーによって処理される前に、リクエストのパスとクエリの部分を変更できます。 ルールは、リクエストの不明化、ウォーターマーキング、HTTPサービスを特定のクライアントIPアドレスに制限するなど、通常はカタログ属性でのみ制御される特定のセキュリティ機能の設定と上書きにも使用できます。

リクエストの前処理ルールは、様々なアプリケーションに適しており、その一部を次に示します。

* 仮想パス *メカニズムを実装し* 、要求パスをファイル、FTP、HTTPパスに再マッピングできるようにします。
* 画像名やパスでフィルタリングされた透かしなど、セキュリティ機能を選択して適用する。
* 特定のIPアドレスからサーバにアクセスする場合に、透かしなどのセキュリティ機能を省略する。
* すべてのリクエストや、URLパスやク `defaultImage=`エリ文字列に特定のパターンを示すリクエストに、などのコマンドを強制的に適用する。
* CPUを大量に消費するコマンドの使用を禁止して、サーバの乱用を防ぎます。
* ソース画像をHTTPまたはFTPサーバー上に配置し、ではなくリクエストパスで指定することを許可しま `src=`す。
* 要求パスまたは画像名に応じて、画質の設定（JPEG画質やシャープなど）を制御します。

ルールセットの作成、使用、管理に関する詳細は、『ルールセットリファレンス』を参 [照してください](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 関連項目 {#see-also}

[ルールセットの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、 [属性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
