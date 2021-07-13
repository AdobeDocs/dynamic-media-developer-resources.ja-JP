---
description: 画像サービングは、正規表現の一致と置換ルールに基づく、シンプルな要求プリプロセッサーを提供します。
solution: Experience Manager
title: 前処理のリクエスト
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 前処理のリクエスト{#request-preprocessing}

画像サービングは、正規表現の一致と置換ルールに基づく、シンプルな要求プリプロセッサーを提供します。

ルール（ルールセット）のコレクションを、デフォルトのカタログを含む各画像カタログに添付できます。 ルールはXML形式のファイルで指定します。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、Platform Serverのパーサーによって処理される前に、リクエストのパスとクエリの部分を変更できます。 ルールは、通常、要求の難読化、ウォーターマーキング、HTTPサービスの特定のクライアントIPアドレスへの制限など、カタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きする場合にも使用できます。

リクエストの前処理ルールは、様々なアプリケーションに適しています。その一部を以下に示します。

* *仮想パス*&#x200B;メカニズムを実装します。これにより、要求パスをファイル、FTP、HTTPパスに再マッピングできます。
* 透かしなどのセキュリティ機能を、画像名またはパスでフィルタリングして選択的に適用する。
* 特定のIPアドレスからサーバーにアクセスする際の透かしなどのセキュリティ機能を省略する。
* `defaultImage=`などのコマンドを、すべてのリクエストまたはURLパスまたはクエリ文字列に特定のパターンを示すリクエストに強制的に適用します。
* CPU負荷の高いコマンドの使用を禁止して、サーバーの乱用を防ぎます。
* ソース画像を`src=`ではなくリクエストパスで指定しながら、HTTPまたはFTPサーバー上に配置できるようにします。
* 要求パスまたは画像名に応じて、画質設定（JPEG画質やシャープなど）を制御します。

ルールセットの作成、使用、管理に関する詳細については、「[ルールセットのリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)」を参照してください。

## 関連項目 {#see-also}

[ルールセットの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、 [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
