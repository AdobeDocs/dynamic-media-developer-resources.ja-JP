---
title: KnockoutBackgroundOptions
description: 選択した画像の背景をマスク（ノックアウト）します。 このデータタイプを使用すると、他のレイヤーに、被写体画像の外側の透明度でオーバーレイできます。 デフォルトでオフになっているオプションのパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 3%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

選択した画像の背景をマスク（ノックアウト）します。 このデータタイプを使用すると、他のレイヤーに、被写体画像の外側の透明度でオーバーレイできます。

このデータタイプはオプションで、デフォルトではオフです。

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## パラメータ {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>次を設定する場合、 `KnockoutBackgroundOptions` Adobe Experience Managerでは、代わりに次のパラメーターを使用します。
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>例：`kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">使用するコーナーを選択します。 <span class="codeph"> corner</span> では次の値を使用できます。 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 左下</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 右上</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 右下</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 許容値</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">透明度に基づいて画像のエッジから空白を削除するオプションの設定です。 0.0 ～ 1.0 の範囲の値を指定します。次の値を指定します。 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 に設定すると、色が完全に一致します。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1：最も多くの色の違いを有効にします。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ピクセルの透明度を <span class="codeph"><span class="varname"> corner</span></span> 変数を使用します。 この <span class="codeph"> fillMethod</span> では次の値を使用できます。 </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>:指定した角のすべてのピクセルを透明にします。 </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>:一致するすべてのピクセルを、場所に関係なく透明にします。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-28c43baafe85434a9ee9e303ed10569a}

この `KnockoutBackgroundOptions` タイプは次のユーザーが使用します。

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
