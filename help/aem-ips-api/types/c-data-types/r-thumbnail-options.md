---
description: サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプ。
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプ。

構文

## パラメータ {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>ビデオのサムネールに使用するフレームの時間（ビデオ開始からのミリ秒単位）を設定します。 値の範囲は 0 ～ビデオの最後です。 <p>注意：時間を誤って指定した場合は、ビデオの最初のフレームがサムネールに使用されます。 詳しくは、 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```
