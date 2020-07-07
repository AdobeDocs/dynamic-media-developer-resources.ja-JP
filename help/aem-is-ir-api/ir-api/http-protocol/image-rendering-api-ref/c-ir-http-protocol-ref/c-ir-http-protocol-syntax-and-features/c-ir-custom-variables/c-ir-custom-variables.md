---
description: 要求のクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-description: 要求のクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-title: カスタム変数
solution: Experience Manager
title: カスタム変数
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Custom variables{#custom-variables}

要求のクエリ部分とvignette::Modifier文字列には、ユーザ定義の変数を含めることができます。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. 「$」を除く、英数字と安全な文字の任意の組み合わせで構成できます。

** *[!DNL value]* **変数を設定する値（文字列）。

変数は、他のサーバーコマンドと同様に、上記の構文を使用して定義します。 変数は、参照する前に定義する必要があります。 で定義された変数はURLリクエストで参照で `vignette::Modifier` き、その逆も可能です。

>[!NOTE]
>
>*[!DNL value]* は、安全なHTTP送信を目的として、1パスでURLエンコードする必要があります。 HTTP経由で再送信する場合は、重複エンコ *[!DNL value]* ーディングが必要です。 これは、がネストされた外部リクエストに置換さ *[!DNL value]* れた場合の例です。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の$で囲む）を埋め込むことで参照されます。 例えば、コマンド名の後の「=」と、後続の「&amp;」との間、またはリクエストの最後の間にあります。 サーバは、このような$ *[!DNL name]*$の各値をに置き換え *[!DNL string]*&#x200B;ます。 コマンド名（コマンドの等号の前）、および要求のパス部分で$ *[!DNL name]*$が使用されている場合は、置換は行われません。

カスタム変数は入れ子にできません。 内にあるすべての$ *[!DNL name]*$は、代わ *[!DNL string]* りになりません。 例えば、要求フラグメントはに解決 `$var2=apple&$var1=my$var2$tree&text=$var1$` され `text=my$var2$tree`ます。

$は予約文字ではありません。 リクエスト内では、それ以外の場合に発生する可能性があります。 たとえば、は有効なコマンド `src=my$texture$file.tif` です(マテリアルカタログエントリまたはテクスチャファイル名が [!DNL my$texture$file.tif] 存在すると仮定した場合)。ただし、は、数値引数が `wid=$number$``wid=` 必要なため、存在しないと仮定します。
