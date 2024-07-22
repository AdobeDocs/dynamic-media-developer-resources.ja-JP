---
title: clipXPath
description: 反転したレイヤークリップパス。 現在のレイヤの除外クリップ パスを指定します。 clipXPath=で定義された領域内にあるレイヤーの部分は、すべて透明にレンダリングされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

反転したレイヤークリップパス。 現在のレイヤの除外クリップ パスを指定します。 clipXPath=で定義された領域内にあるレイヤーの部分は、すべて透明にレンダリングされます。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>パスデータ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCII のみ）。 </p></td> 
 </tr> 
</table>

[pathName](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) および `*`pathDefinition`*` の説明など、追加情報については、`*`clipPath`*` を参照してください。

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 `clipPath=` が指定されていない場合、無視されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
