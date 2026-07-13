---
title: カスタム変数
description: リクエストおよびビネット修飾子文字列のクエリ部分には、ユーザー定義の変数が含まれる場合があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
TQID: 'https://experienceleague.adobe.com/1-o3GqgzwvPYV8UDBuZu5udOiG-p8Tue3Fo-ft8-QhI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 0%

---

# カスタム変数{#custom-variables}

リクエストおよびビネット：：修飾子文字列のクエリ部分には、ユーザー定義の変数が含まれる場合があります。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` – 変数名。 `$`を除く、アルファ、数字、および安全な文字の任意の組み合わせで構成できます。

`[!DNL value]` – 変数を設定する値（文字列）。

変数は、上記の構文を使用して、他のサーバーコマンドと同様に定義されます。 変数を参照する前に、変数を定義する必要があります。 `vignette::Modifier`で定義された変数は、URL リクエストで参照でき、逆に参照できます。

>[!NOTE]
>
>`[!DNL value]`は、安全なHTTP送信のためにシングルパス URL エンコードする必要があります。 `[!DNL value]`がHTTP経由で再送信される場合は、ダブルエンコーディングが必要です。 この状況は、`[!DNL value]`がネストされた外部リクエストに置き換えられた場合に発生します。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の`$`で囲まれた）を埋め込むことで参照されます。 例えば、コマンド名に続く`=`と、その後の`&`またはリクエストの最後の間です。 サーバーは、そのような発生のそれぞれを`$ [!DNL name]$`に`[!DNL string]`に置き換えます。 コマンド名（コマンドの等号の前）およびリクエストのパス部分で`$ [!DNL name]$`が発生しても、置換は行われません。

カスタム変数はネストできません。 `[!DNL string]`内の`$ [!DNL name]$`の出現箇所は置換されません。 例えば、リクエストフラグメント `$var2=apple&$var1=my$var2$tree&text=$var1$`は`text=my$var2$tree`に解決されます。

`$`は予約済みの文字ではありません。リクエストで他の文字が発生する可能性があります。 例えば、`src=my$texture$file.tif`は有効なコマンドです（`[!DNL my$texture$file.tif]`という名前のマテリアルカタログエントリまたはテクスチャファイルが存在すると仮定します）。一方、`wid=$number$`はそうではありません。`wid=`には数値引数が必要です。

