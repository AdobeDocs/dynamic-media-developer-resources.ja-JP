---
description: eCatalogビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---

# setParams{#setparams}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL ` setParams( *`params`*)`]

1つ以上のパラメーターに指定した値を設定します。 メソッド引数の構文は、URLクエリ文字列と同じです。 つまり、name=valueのペアを[!DNL `&`]で区切って表します。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセントでエンコードされます。 [!DNL `init()`]を呼び出す前に、このパラメーターを呼び出す必要があります。

ビューアの設定情報が[!DNL `config`] JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valueパラメーターのペアを&amp;で区 <span class="codeph"> 切ります</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
