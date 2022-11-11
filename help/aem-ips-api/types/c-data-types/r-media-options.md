---
description: ビデオのサムネール画像を生成します。
solution: Experience Manager
title: MediaOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# [!DNL MediaOptions]{#mediaoptions}

ビデオのサムネール画像を生成します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">の配列 <span class="codeph"> プロパティセット</span> は、ビデオのトランスコード用のビデオエンコーディングプリセットの参照を処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> true の場合、ビデオの最初のフレームが抽出され、サムネール画像として使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ThumbnailOptions</span> </td> 
   <td colname="col3">（オプション）特定のビデオフレームを選択して、サムネール画像として使用できます。 <p>サムネール画像を指定するには、使用するフレームの時間 ( ビデオ開始からの時間（ミリ秒）) を渡します。 値の範囲は 0 ～ビデオの最後です。 <p>注意：時刻を正しく指定しない場合、 <span class="codeph"> generateThumbnail</span> デフォルトは true です。 </p></p><p>詳しくは、 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-87cb83407198432c95eaa2db9f12f9db}

この `mediaOptions` タイプは次のユーザーが使用します。

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
