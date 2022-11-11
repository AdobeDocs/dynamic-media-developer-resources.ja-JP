---
description: 画像サービングは、正規表現の一致と置き換えルールに基づく、シンプルなリクエストプリプロセッサーを提供します。
solution: Experience Manager
title: 前処理をリクエスト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 前処理をリクエスト{#request-preprocessing}

画像サービングは、正規表現の一致と置き換えルールに基づく、シンプルなリクエストプリプロセッサーを提供します。

ルール（ルールセット）のコレクションを、デフォルトのカタログを含む各画像カタログに添付できます。 ルールは XML 形式のファイルで指定します。

リクエストの前処理ルールは、リクエストが [!DNL Platform Server]パスの操作、コマンドの追加、コマンド値の変更、テンプレートまたはマクロの適用を含むのパーサー。 また、ルールを使用して、要求の難読化、ウォーターマークなど、通常はカタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きし、HTTP サービスを特定のクライアント IP アドレスに制限することもできます。

リクエストの前処理ルールは、様々なアプリケーションに適しています。一部は次のとおりです。

* の実装 *仮想パス* メカニズム：要求パスをファイル、FTP、HTTP パスに再マッピングできます。
* 透かしなどのセキュリティ機能を、画像名またはパスでフィルタリングして、選択的に強制します。
* 特定の IP アドレスからサーバーにアクセスする際に、透かしや他のセキュリティ機能を省略する。
* 次のようなコマンドの適用を強制 `defaultImage=`を、URL パスまたはクエリ文字列に特定のパターンを示すすべてのリクエストまたはリクエストに対して適用できます。
* CPU 負荷の高いコマンドを使用してサーバの乱用を防ぐことを禁止します。
* ソース画像を HTTP または FTP サーバー上に配置し、リクエストパス上で指定する ( `src=`.
* 要求パスまたは画像名に応じて、画質設定 (JPEGの画質やシャープニングなど ) を制御します。

ルールセットの作成、使用、管理について詳しくは、 [ルールセットの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## 関連項目 {#see-also}

[ルールセットの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
