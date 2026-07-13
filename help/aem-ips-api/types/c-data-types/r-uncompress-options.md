---
title: UnCompressOptions
description: アップロード設定を使用すると、ZIP ファイルやTAR ファイルをプライマリアセットとして処理したり（なし）、コンテンツを抽出してアップロードしたりできます（非圧縮）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
TQID: 'https://experienceleague.adobe.com/eVVqmW5DXCojZTIPk-4HRaclyVVY1uOf1rt6VnvyCUc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 4%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

アップロード設定を使用すると、ZIP ファイルやTAR ファイルをプライマリアセットとして処理したり（なし）、コンテンツを抽出してアップロードしたりできます（非圧縮）。

>[!NOTE]
>
>設定`None`がデフォルトです。

## パラメーター {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> プロセス </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ZIPおよびTAR アーカイブファイルの処理を制御します。 2つのオプションが用意されています。 <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph">なし：</span> プライマリアセットとして処理します。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph">圧縮を解除：</span>内容を抽出して処理します。 </li>
     </ul><p>注意：文字列定数では大文字と小文字が区別されます。 <span class="codeph">非圧縮</span>または<span class="codeph">非圧縮</span>ではなく、<span class="codeph">非圧縮</span>を使用します。 </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-b2a829cf5511412e968bb2000f85cc31}

`unCompressionOptions` タイプは次のユーザーによって使用されます：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

