---
description: 最適化されたピラミッド TIF ファイルの画像のシャープネスを向上させるための設定。
solution: Experience Manager
title: アンシャープマスクオプション
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 8%

---

# [!DNL UnsharpMaskOptions]{#unsharpmaskoptions}

最適化されたピラミッド TIF ファイルの画像のシャープネスを向上させるための設定。

`unsharpMaskOptions=[ *` 量、半径、しきい値、モノクロ `*]`

## パラメーター {#section-c3f0d03136ba4422819cb463bd393885}

`unsharpMaskOptions`n`minOccurs=" *` を使用してオプション `*".` 値を指定します

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 名前 </th>
   <th colname="col2" class="entry"> 種類 </th>
   <th colname="col3" class="entry"> 説明 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 値</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>端のピクセルに適用されるコントラストを制御します。 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">範囲：0.0 ～ 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">デフォルト：0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 半径</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>画像のエッジの周囲のピクセル数を設定してシャープネスを制御します。 適切な値は、画像のサイズに依存します。 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">範囲：0.0 ～ 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">値を小さくすると、エッジのピクセルのみがシャープになります。 </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">値を大きくすると、ピクセルの幅が広くなります。 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> しきい値</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>周囲の領域と異なるピクセルをエッジピクセルと見なしてシャープにする方法を決定します。 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">範囲：0～255 （整数のみ）。 </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">デフォルト：6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> モノクロ</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>値には、<span class="codeph"> 0</span> または <span class="codeph"> 1</span> のみが含まれます。 </p><p>各色成分に個別に適用する場合は <span class="codeph"> 0</span> に、画像の明るさ（強さ）にのみ適用する場合は <span class="codeph"> 1</span> に設定します。 レイヤーマスクまたはコンポジットマスクもシャープになります。 </p><p>モノクロ <span class="codeph"><span class="varname"> は </span></span> グレースケール画像では無視されます。 </p></td>
  </tr>
 </tbody>
</table>

## 例 {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## 使用者 {#section-db8124a5468b498694a780f8a56a4560}

`unsharpMaskOptions` のタイプは、次のユーザーが使用します。

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [ 画像サービス API リファレンス：op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html?lang=ja)
