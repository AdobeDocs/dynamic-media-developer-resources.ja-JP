---
title: コマンドマクロ
description: コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** マクロ名

マクロは個別のマクロ定義ファイルで定義され、マテリアル カタログまたは既定のカタログに添付できます。

*[!DNL name]*&#x200B;は大文字と小文字を区別せず、ASCII文字、数字、「 – 」、「_」、「。」の組み合わせで構成できます。

「?」の後のリクエスト内の任意の場所、または`vignette::Modifier` フィールド内の任意の場所でマクロを呼び出します。 マクロは、1つ以上の画像レンダリングコマンドのみを表すことができ、「&amp;」区切り記号を使用して他のコマンドから区切る必要があります。

マクロ呼び出しは、パースの早い段階で代用文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 このワークフローは、`vignette::Modifier`とは異なります。リクエスト文字列内のコマンドは、リクエスト内の位置にかかわらず、`vignette::Modifier`文字列内のコマンドを上書きします。

コマンドマクロには引数の値を指定できませんが、カスタム変数を使用して、リクエストの値をマクロに渡すことができます。

マクロはネストできません。

**例**

マクロは、同じコマンドまたは属性を異なるレンダリング画像に適用する場合に便利です。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

共通の属性のマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

マクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

`qlt=`は3番目のリクエストとは異なるため、マクロが呼び出された後にソフトウェアが値を上書きします（`qlt=` *before* `$render$`の指定は無効です）。

**関連項目**

`catalog::MacroFile`、`catalog::Modifier`、マクロ定義参照

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

