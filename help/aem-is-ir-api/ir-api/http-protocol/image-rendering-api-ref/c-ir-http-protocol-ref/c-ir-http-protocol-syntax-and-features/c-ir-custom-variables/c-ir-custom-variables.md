---
title: カスタム変数
description: リクエストのクエリ部分とビネット修飾子文字列には、ユーザ定義変数を含めることができます。
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

requests と vignette::Modifier 文字列の query 部分には、ユーザ定義変数を含めることができます。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]`  — 変数名。 英字、数字、安全な文字の組み合わせで構成することができます ( `$`.

`[!DNL value]`  — 変数を設定する値（文字列）。

変数は、上記の構文を使用して、他のサーバーコマンドと同様に定義されます。 変数を参照する前に、変数を定義する必要があります。 で定義される変数 `vignette::Modifier` は URL リクエストで参照することも、逆に参照することもできます。

>[!NOTE]
>
>`[!DNL value]` は、安全な HTTP 送信を目的として、1 パスで URL エンコードする必要があります。 次の場合は二重エンコーディングが必要です `[!DNL value]` は、HTTP を介して再送信されます。 この状況は、 `[!DNL value]` は、ネストされた外部リクエストに置き換えられます。

変数は、変数名を埋め込むことで参照されます ( 先頭と末尾に `$`) をコマンド値の任意の場所に配置します。 例えば、 `=`  コマンド名とその後の `&` またはリクエストの終わり。 サーバは、このような `$ [!DNL name]$` と `[!DNL string]`. 置換は `$ [!DNL name]$` コマンド名（コマンドの等号の前）とリクエストのパス部分。

カスタム変数はネストできません。 次のいずれかの `$ [!DNL name]$` 範囲 `[!DNL string]` は置換されません。 例えば、要求フラグメントなどです。 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解決済み `text=my$var2$tree`.

`$` は予約文字ではありません。リクエストで別の場合に発生する可能性があります。 例： `src=my$texture$file.tif` は有効なコマンドです ( マテリアルカタログのエントリまたはテクスチャファイルが `[!DNL my$texture$file.tif]` が存在する )、 `wid=$number$` がではないのは、 `wid=` には数値引数が必要です。
