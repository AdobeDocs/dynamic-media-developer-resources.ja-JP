---
title: defaultImage
description: デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。

` defaultImage= *`オブジェクト`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
</table>

*`object`* は、カタログエントリ（テンプレートを含む）または単純な画像ファイルパスです。 見つからない画像をデフォルトの画像で置き換えるのに役立ちます。 この値は、対応するカタログの値を上書きします `attribute::DefaultImage`. 空の値 ( `defaultImage=`) を指定すると、デフォルトの画像処理が無効になります。

>[!NOTE]
>
>デフォルトのイメージメカニズムは、SVGオブジェクトには適用されません。 リクエストで指定されたSVGオブジェクトが見つからない場合は、エラーが返されます。

次の場合 `attribute::DefaultImageMode=0`, *`object`* マルチ画像合成で 1 つの画像のみが欠落している場合でも、元のリクエスト全体を置き換えます。 元の要求から保持されるコマンドは次のとおりです。 `wid=`, `hei=`, `fmt=`, `qlt=`.

次の場合 `attribute::DefaultImageMode=1`を指定した場合、見つからないレイヤイメージのみがオブジェクトに置き換えられます。見つからないレイヤの属性が適用され、合成が通常どおり処理されて返されます。

## プロパティ {#section-d30923d8dc4042eba10989212dd70887}

要求属性。 現在の画層設定に関係なく適用されます。 次の場合は無視 `req=` 次の値以外： `img` または `tmb`.

## 制限事項 {#section-30df31bc8cac41cd917f1e45196779c2}

外部の画像ソースは、デフォルトの画像メカニズムの対象にはなりません。外部の画像ソースが有効でない場合は、エラーが返されます。

画像サービングがに戻ります。 `DefaultImageMode=0` ネストされた画像レンダリングまたは FXG レンダリング要求が失敗した場合。

## 初期設定 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage` をクリックします。

## 関連項目 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
