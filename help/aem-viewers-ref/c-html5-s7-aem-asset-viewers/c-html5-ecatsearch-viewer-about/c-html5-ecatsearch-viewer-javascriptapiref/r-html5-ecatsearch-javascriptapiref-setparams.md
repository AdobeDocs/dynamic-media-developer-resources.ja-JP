---
description: eCatalog ビューアのJavaScript API リファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

eCatalog ビューアのJavaScript API リファレンス。

[!DNL ` setParams( *`params`*)`]

1 つ以上のパラメーターを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、名前=値のペアを [!DNL `&`] で区切って表します。 クエリ文字列の場合と同様に、名前と値は UTF8 を使用してパーセント エンコードされます。 を呼び出す前に、このパラメーター [!DNL `init()`] 呼び出す必要があります。

ビューアの設定情報が JSON オブジェクトとともにコンストラクターに渡され [!DNL `config`] 場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> {string}</span> name=value パラメーターのペアを <span class="codeph"> &amp;</span> で区切って <span class="codeph"> 定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
