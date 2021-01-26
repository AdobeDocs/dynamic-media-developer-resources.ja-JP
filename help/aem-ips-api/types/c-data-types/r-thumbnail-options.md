---
description: サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプです。
seo-description: サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプです。
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Dynamic Media Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# ThumbnailOptions{#thumbnailoptions}

サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプです。

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
   <td colname="col3"> <p>ビデオサムネールに使用するフレームの時間(ビデオ開始からの経過時間)をミリ秒単位で設定します。 値の範囲は0 ～ビデオの最後です。 <p>注意：時間を誤って指定した場合は、ビデオの最初のフレームがサムネールに使用されます。 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>を参照してください。 </p></p> </td> 
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

