---
description: 画像サービングは、正規表現の一致と置換ルールに基づいて、シンプルなリクエストプリプロセッサーを提供します。
solution: Experience Manager
title: リクエストの前処理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# リクエストの前処理{#request-preprocessing}

画像サービングは、正規表現の一致と置換ルールに基づいて、シンプルなリクエストプリプロセッサーを提供します。

デフォルトのカタログを含め、各画像カタログにルールのコレクション（ルールセット）を添付できます。 ルールは、XML 形式のファイルで指定します。

リクエスト前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リク [!DNL Platform Server] ストのパーサーで処理される前に、リクエストのパスとクエリの部分を変更できます。 また、ルールを使用して、通常はカタログ属性でのみ制御される特定のセキュリティ機能（リクエストの不明化、ウォーターマーキング、特定のクライアント IP アドレスへの HTTP サービスの制限など）を設定および上書きすることもできます。

リクエストの前処理ルールは様々なアプリケーションに適しています。その一部を次に示します。

* リクエストパスをファイル、FTP、HTTP の各パスに再マッピングできる *仮想パス* メカニズムを実装する。
* 画像の名前またはパスでフィルタリングした、透かしなどのセキュリティ機能を選択的に適用する。
* 特定の IP アドレスからサーバーにアクセスする際に、透かしなどのセキュリティ機能を省略する。
* `defaultImage=` などのコマンドを、すべてのリクエストまたは URL パスやクエリ文字列に特定のパターンを示すリクエストに強制的に適用します。
* サーバーの不正使用を防ぐために、CPUで集中的に使用するコマンドの使用を許可しない。
* ソース画像を `src=` ではなくリクエストパスで指定しながら、HTTP サーバーまたは FTP サーバーに配置できるようにします。
* リクエストパスまたは画像名に応じて、画質の設定（JPEG画質やシャープニングなど）を制御します。

ルールセットの作成、使用および管理について詳しくは、[ ルールセット参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) を参照してください。

## 関連項目 {#see-also}

[ 規則セットの参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
