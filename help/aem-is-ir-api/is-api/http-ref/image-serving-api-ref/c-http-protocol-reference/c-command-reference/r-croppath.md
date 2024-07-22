---
title: cropPathE
description: 埋め込まれた名前付きパスのバウンディングボックスをトリミングできます。 この切り抜きは、画像のサイズを変更します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# cropPathE{#croppathe}

埋め込まれた名前付きパスのバウンディングボックスをトリミングできます。 この切り抜きは、画像のサイズを変更します。

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCII のみ）。 </p> <p> pathName</span></span><span class="codeph"><span class="varname">、レイヤーソース画像に埋め込まれたパスの名前です。 パスは、画像コンテンツとの相対的な整合性を維持するために、必要に応じて自動的に変換されます。 複数の <span class="codeph"><span class="varname"> pathName</span></span> が指定されている場合、サーバーは各パスのバウンディングボックスまで 1 つずつ切り抜きます。 ソース画像に見つからない <span class="codeph"><span class="varname"> pathName</span></span> は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。

指定した名前のパスがレイヤーソースイメージに見つからない場合、またはレイヤーソースがイメージでない場合、`cropPathE=` は無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし。レイヤーをさらに切り抜きません。

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
