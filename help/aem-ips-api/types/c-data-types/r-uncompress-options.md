---
description: ZIP ファイルと TAR ファイルをプライマリアセットとして処理する（なし）か、その内容を抽出してアップロードする (UnCompress) ための設定をアップロードします。
solution: Experience Manager
title: UnCompressOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 5%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

ZIP ファイルと TAR ファイルをプライマリアセットとして処理する（なし）か、その内容を抽出してアップロードする (UnCompress) ための設定をアップロードします。

>[!NOTE]
>
>`None` がデフォルトです。

## パラメータ {#section-10e49e27f60743da970a4ff1c4587eab}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> プロセス</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ZIP および TAR アーカイブファイルの処理を制御します。 次の 2 つのオプションを提供します。 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> なし：</span> プライマリアセットとして処理します。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> 解凍：</span> コンテンツを抽出して処理します。 </li>
     </ul><p>注意：文字列定数では大文字と小文字が区別されます。 用途 <span class="codeph"> 解凍</span>ではない <span class="codeph"> 解凍</span> または <span class="codeph"> unCompress</span>. </p></p> </td> 
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

この `unCompressionOptions` タイプは次のユーザーが使用します。

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
