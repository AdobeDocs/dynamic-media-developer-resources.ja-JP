---
description: サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプです。
seo-description: サムネール画像として使用する特定のビデオフレームを選択できるオプションのタイプです。
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Scene7 Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>ビデオサムネールに使用するフレームの時間（ビデオ開始からのミリ秒）を設定します。 値の範囲は0 ～ビデオの最後です。 <p>注意：時間を正しく指定しなかった場合、ビデオの最初のフレームがサムネールに使用されます。 詳しくは、MediaOptionsを参 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 照してくださ</a>い。 </p></p> </td> 
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

