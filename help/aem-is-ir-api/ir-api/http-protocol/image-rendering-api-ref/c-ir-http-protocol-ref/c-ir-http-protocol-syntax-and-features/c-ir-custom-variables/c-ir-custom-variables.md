---
description: 要求のクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-description: 要求のクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-title: カスタム変数
solution: Experience Manager
title: カスタム変数
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# カスタム変数{#custom-variables}

要求のクエリ部分とvignette::Modifier文字列には、ユーザ定義の変数を含めることができます。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **変数名。 「$」を除く、英数字と安全な文字の任意の組み合わせで構成できます。

** *[!DNL value]* **変数の設定先の値（文字列）

変数は、他のサーバーコマンドと同様に、上記の構文を使用して定義します。 変数は、参照する前に定義する必要があります。 `vignette::Modifier`に定義された変数はURLリクエストで参照でき、逆も同様です。

>[!NOTE]
>
>*[!DNL value]* は、安全なHTTP送信を目的として、1パスでURLエンコードする必要があります。*[!DNL value]*&#x200B;がHTTP経由で再送信される場合は、重複エンコーディングが必要です。 これは、*[!DNL value]*&#x200B;が入れ子になった外部要求に置き換えられる場合の例です。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の$で囲む）を埋め込むことで参照されます。 例えば、コマンド名の後の「=」と、後続の「&amp;」との間、またはリクエストの最後の間にあります。 サーバは、このような$ *[!DNL name]*$を&#x200B;*[!DNL string]*&#x200B;で置き換えます。 コマンド名（コマンドの等号の前）、および要求のパス部分の$ *[!DNL name]*$が存在する場合は、置換は行われません。

カスタム変数は入れ子にできません。 *[!DNL string]*&#x200B;内の$ *[!DNL name]*$は置換されません。 例えば、リクエストフラグメント`$var2=apple&$var1=my$var2$tree&text=$var1$`は`text=my$var2$tree`に解決されます。

$は予約文字ではありません。リクエスト内では、それ以外の場合に発生する可能性があります。 例えば、`src=my$texture$file.tif`は有効なコマンドです（[!DNL my$texture$file.tif]という名前のマテリアルカタログエントリまたはテクスチャファイルが存在する場合）。`wid=$number$`は、`wid=`には数値引数が必要なので、存在しません。
