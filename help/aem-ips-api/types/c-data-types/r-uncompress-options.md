---
description: アップロード設定を使用して、ZIPファイルとTARファイルをプライマリアセットとして処理（なし）、またはその内容を抽出してアップロード（解凍）します。
solution: Experience Manager
title: UnCompressOptions
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 5%

---


# UnCompressOptions{#uncompressoptions}

アップロード設定を使用して、ZIPファイルとTARファイルをプライマリアセットとして処理（なし）、またはその内容を抽出してアップロード（解凍）します。

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
   <td colname="col3"> <p>ZIPおよびTARアーカイブファイルの処理を制御します。 次の2つのオプションを提供します。 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> なし：プライマリアセット</span> として処理します。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> 解凍：内容を</span> 抽出して処理します。 </li>
     </ul><p>注意：文字列定数では大文字と小文字が区別されます。 <span class="codeph"> uncompress</span>や<span class="codeph"> unCompress</span>ではなく、<span class="codeph"> UnCompress</span>を使用します。 </p></p> </td> 
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

## {#section-b2a829cf5511412e968bb2000f85cc31}が使用

`unCompressionOptions`型は次のユーザーが使用します。

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

