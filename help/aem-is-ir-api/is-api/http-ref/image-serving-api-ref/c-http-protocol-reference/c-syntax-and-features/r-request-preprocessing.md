---
description: 画像サービングは、正規表現の一致ルールと置換ルールに基づくシンプルなリクエストプリプロセッサを提供します。
solution: Experience Manager
title: リクエストの前処理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
TQID: 'https://experienceleague.adobe.com/My4SapYE0s9rFPPP6kSThzJ5--N6H7EUOuxC-M-xyrk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 288
ht-degree: 0%

---

# リクエストの前処理{#request-preprocessing}

画像サービングは、正規表現の一致ルールと置換ルールに基づくシンプルなリクエストプリプロセッサを提供します。

ルールのコレクション（ルールセット）は、デフォルトカタログを含む各画像カタログに添付できます。 ルールは、XML形式のファイルで指定します。

リクエスト前処理ルールは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、[!DNL Platform Server]のパーサーによって処理される前に、リクエストのパスとクエリ部分を変更できます。 また、ルールを使用して、リクエストの難読化、ウォーターマーク、HTTP サービスの特定のクライアント IP アドレスへの制限など、通常はカタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きすることもできます。

リクエスト前処理ルールは、以下に示すさまざまなアプリケーションに適しています。

* *仮想パス* メカニズムを実装します。これにより、リクエストパスをファイル、FTP、およびHTTP パスに再マッピングできます。
* 透かしなどのセキュリティ機能を、画像名やパスでフィルタリングして選択的に適用します。
* 特定のIP アドレスからサーバーにアクセスする際に、透かしやその他のセキュリティ機能を省略する。
* すべてのリクエスト、またはURL パスまたはクエリ文字列に特定のパターンを示すリクエストに`defaultImage=`などのコマンドを強制的に適用します。
* サーバーの不正使用を防ぐために、CPUを多用するコマンドの使用を禁止します。
* ソースイメージを`src=`ではなくリクエストパスで指定しながら、HTTP サーバーまたはFTP サーバーに配置できるようにします。
* リクエストパスや画像名に応じて、画質の設定（JPEG画質やシャープニングなど）を制御します。

ルールセットの作成、使用、管理に関する詳細については、[&#x200B; ルールセット参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)を参照してください。

## 関連項目 {#see-also}

[&#x200B; ルールセット参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、[属性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
