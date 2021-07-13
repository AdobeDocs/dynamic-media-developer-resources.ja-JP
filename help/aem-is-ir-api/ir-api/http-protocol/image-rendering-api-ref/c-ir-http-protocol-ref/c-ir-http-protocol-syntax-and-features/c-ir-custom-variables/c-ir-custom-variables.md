---
description: リクエストのクエリ部分とビネット修飾子文字列には、ユーザ定義変数を含めることができます。
solution: Experience Manager
title: カスタム変数
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# カスタム変数{#custom-variables}

requestsとvignette::Modifier文字列のクエリ部分には、ユーザ定義変数を含めることができます。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **変数名。 「$.」を除く、任意の英字、数字、および安全な文字の組み合わせで構成することができます。

** *[!DNL value]* **変数の設定先の値（文字列）。

変数は、上記の構文を使用して、他のサーバーコマンドと同様に定義されます。 変数を参照する前に、変数を定義する必要があります。 `vignette::Modifier`で定義された変数はURLリクエストで参照でき、逆も可能です。

>[!NOTE]
>
>*[!DNL value]* は、安全なHTTP送信を実現するために、1パスでURLエンコードする必要があります。*[!DNL value]*&#x200B;がHTTP経由で再送信される場合は、二重エンコーディングが必要です。 これは、*[!DNL value]*&#x200B;がネストされた外部要求に置き換えられる場合に発生します。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の$で囲む）を埋め込むことで参照されます。 例えば、コマンド名の後の「=」と、後続の「&amp;」またはリクエストの最後の間。 サーバは、$ *[!DNL name]*$を&#x200B;*[!DNL string]*&#x200B;に置き換えます。 コマンド名（コマンドの等号の前）と要求のパス部分で$ *[!DNL name]*$が存在する場合は、置換は行われません。

カスタム変数はネストできません。 *[!DNL string]*&#x200B;内の$ *[!DNL name]*$は置き換えられません。 例えば、要求フラグメント`$var2=apple&$var1=my$var2$tree&text=$var1$`は`text=my$var2$tree`に解決されます。

$は予約文字ではありません。リクエスト内で別の場合に発生する可能性があります。 例えば、`src=my$texture$file.tif`は有効なコマンドです（[!DNL my$texture$file.tif]という名前のマテリアルカタログエントリまたはテクスチャファイルが存在する場合）が、`wid=$number$`は有効ではありません。`wid=`には数値引数が必要です。
