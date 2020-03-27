---
description: リクエストのクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-description: リクエストのクエリ部分とビネット修飾子の文字列には、ユーザ定義の変数を含めることができます。
seo-title: カスタム変数
solution: Experience Manager
title: カスタム変数
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Custom variables{#custom-variables}

リクエストのクエリ部分とvignette::Modifier文字列には、ユーザ定義の変数を含めることができます。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. 「$」を除く任意の英数字、数字、安全な文字の組み合わせで構成できます。

** *[!DNL value]* **変数の設定先の値（文字列）。

変数は、他のサーバーコマンドと同様に、上記の構文を使用して定義します。 変数を参照する前に、変数を定義する必要があります。 で定義された変数はURL `vignette::Modifier` リクエストで参照でき、逆も同様です。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>*[!DNL value]* は、安全なHTTP送信を目的として、シングルパスURLエンコードする必要があります。 HTTP経由で再送信する場合は、二重エ *[!DNL value]* ンコーディングが必要です。 これは、がネストされた外部 *[!DNL value]* リクエストに置き換えられる場合です。

変数は、コマンド値の任意の場所に変数名（先頭と末尾の$で囲まれる）を埋め込むことで参照されます。 例えば、コマンド名の後の「=」と、後続の「&amp;」、またはリクエストの最後の間で使用します。 サーバは、このような$$の各値をに置き *[!DNL name]*&#x200B;換えま *[!DNL string]*&#x200B;す。 コマンド名（コマンドの等号の前）および要求のパス部分で$ *[!DNL name]*$が出現した場合、置換は行われません。

カスタム変数は入れ子にできません。 内のすべての$ *[!DNL name]*$は置換 *[!DNL string]* されません。 例えば、リクエストフラグメントはに解決 `$var2=apple&$var1=my$var2$tree&text=$var1$` されるとしま `text=my$var2$tree`す。

$は予約文字ではありません。リクエスト内で発生する可能性があります。 たとえば、は有効 `src=my$texture$file.tif` なコマンド（という名前のマテリアルカタログエントリまたはテクスチャファイルが存在すると仮定）ですが、は、数 [!DNL my$texture$file.tif] 値引数が必要なので、は存在し `wid=$number$` ないと仮定 `wid=` しています。
