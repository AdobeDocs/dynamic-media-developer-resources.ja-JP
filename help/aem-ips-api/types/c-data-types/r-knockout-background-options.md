---
description: 選択した画像の背景をマスク（ノックアウト）します。 これにより、他のレイヤーの中で、被写体の画像の外側に透明部分を持つレイヤーを重ね合わせることができます。 デフォルトではオフのオプションのパラメーター。
seo-description: 選択した画像の背景をマスク（ノックアウト）します。 これにより、他のレイヤーの中で、被写体の画像の外側に透明部分を持つレイヤーを重ね合わせることができます。 デフォルトではオフのオプションのパラメーター。
seo-title: KnockoutBackgroundOptions
solution: Experience Manager
title: KnockoutBackgroundOptions
topic: Scene7 Image Production System API
uuid: 1486d646-f42a-4ed4-9450-313950969c39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# KnockoutBackgroundOptions{#knockoutbackgroundoptions}

選択した画像の背景をマスク（ノックアウト）します。 これにより、他のレイヤーの中で、被写体の画像の外側に透明部分を持つレイヤーを重ね合わせることができます。 デフォルトではオフのオプションのパラメーター。

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## パラメータ {#section-3149b49ccb714e6eafa6655354816819}

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
   <td colname="col3">操作するコーナーを選択します。 <span class="codeph"> 次の値は</span> cornerで受け付けます。 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 左下</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 右上</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 右下</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 耐性</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:重複</span> </td> 
   <td colname="col3">透明度に基づいて画像の境界線から空白を削除するオプションの設定です。 0.0 ～ 1.0の範囲の値を指定できます。次を指定します。 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0の場合、色が完全に一致します。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1を指定すると、最も多くの色の違いが有効になります。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><span class="codeph"><span class="varname"> corner</span></span>変数で指定された場所のピクセル透明度を制御します。 <span class="codeph"> fillMethod</span>は次の値を受け付けます。 </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>:指定した隅のすべてのピクセルを透明にします。 </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>:一致するすべてのピクセルを、場所を問わず透明にします。 </li> 
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

## {#section-28c43baafe85434a9ee9e303ed10569a}が使用

`KnockoutBackgroundOptions`型は次のユーザーが使用します。

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

