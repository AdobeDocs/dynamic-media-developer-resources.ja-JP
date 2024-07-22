---
title: カスタム変数
description: リクエストおよびビネット修飾子の文字列のクエリ部分には、ユーザー定義変数を含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# カスタム変数{#custom-variables}

リクエストおよびビネット：:Modifier 文字列のクエリ部分には、ユーザー定義の変数を含めることができます。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` – 変数名。 `$` を除く、英数字、安全文字の任意の組み合わせで構成される場合があります。

`[!DNL value]` – 変数を設定する値（文字列）。

変数は、上記の構文を使用して、他のサーバーコマンドと同様に定義されます。 変数は、参照する前に定義する必要があります。 `vignette::Modifier` で定義された変数は、URL リクエストで参照できます。逆の場合も同じです。

>[!NOTE]
>
>安全な HTTP 送信を行うには、`[!DNL value]` をシングルパス URL エンコードする必要があります。 HTTP 経由で再送信する場合 `[!DNL value]` ダブルエンコーディングが必要です。 このような状況は、`[!DNL value]` がネストされた外部リクエストに置き換えられた場合です。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の `$` で囲まれた名前）を埋め込むことで参照されます。 例えば、コマンド名の後の `=` と、後続の `&` またはリクエストの終わり。 サーバーは、このような `$ [!DNL name]$` の発生をそれぞれ `[!DNL string]` で置き換えます。 コマンド名（コマンドの等号の前）およびリクエストのパス部分で `$ [!DNL name]$` が使用されていても、置き換えは行われません。

カスタム変数はネストできません。 `[!DNL string]` 内の `$ [!DNL name]$` に一致する語句は置換されません。 例えば、リクエストフラグメント `$var2=apple&$var1=my$var2$tree&text=$var1$` は `text=my$var2$tree` に解決されます。

`$` は予約文字ではありません。それ以外の場合はリクエストで発生する可能性があります。 たとえば、`src=my$texture$file.tif` は有効なコマンドですが（`[!DNL my$texture$file.tif]` という名前のマテリアル カタログ エントリまたはテクスチャ ファイルが存在すると仮定）、`wid=$number$` は有効ではありません。`wid=` には数値の引数が必要です。
