---
description: PDF ジョブオプションを適用します。 ジョブオプションファイルまたはPDF プリセットは、「PDFとして保存」オプションダイアログまたはInDesignのPDF プリセットでIllustratorによって生成されるファイルです。
solution: Experience Manager
title: joboption
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e7224e7-d801-4550-b95e-24d15734043a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 38%

---

# joboption{#joboption}

PDF ジョブオプションを適用します。 ジョブオプションファイルまたはPDF プリセットは、「PDFとして保存」オプションダイアログまたはInDesignのPDF プリセットでIllustratorによって生成されるファイルです。

` joboption= *` 値 `*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 値 </span></span> </p> </td> 
  <td class="stentry"> <p>ジョブオプションファイルの IPSID。 </p></td> 
 </tr> 
</table>

ジョブオプションファイルは、IPS/Dynamic Media Classicでアップロードおよび公開できます。 ジョブオプションファイルに含まれるPDF オプションは、PDFの生成時に使用されます。

現在、次のオプションがサポートされています。

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般 </p></td> 
  <td class="stentry"> <p> 互換性のある形式 </p> <p> オブジェクトレベルの圧縮 </p> <p> サムネールを埋め込み </p> <p> Web 表示用に最適化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>画像 </p></td> 
  <td class="stentry"> <p> カラー、グレー、モノラルのダウンサンプル、解像度、しきい値、圧縮 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>フォント </p></td> 
  <td class="stentry"> <p> すべてのフォントを埋め込む </p> <p> OpenType フォントを埋め込む </p> <p> 使用している文字の割合が次より少ない場合サブセットフォントにする： </p> <p> 常に埋め込むフォントのリスト </p> <p> 常に埋め込まないフォントのリスト </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>カラー </p></td> 
  <td class="stentry"> <p> カラー戦略（画像にタグ付けするだけでは、すべてをタグ付けとして扱われます） </p> <p> 文書レンダリングインテント </p> <p> 4.2.5 では、次の作業スペースのみがサポートされます。 </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB、エンコーディング範囲指定あり［-4.0 ～ 4.0］ </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Flat XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">Linear ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8-bit </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8-bit </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">グレー <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Gray Gamma 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Gray Gamma 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Dot Gain 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Dot Gain 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Dot Gain 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Dot Gain 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Dot Gain 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> キャリブレーションされた CMYK カラースペースの CMYK を維持 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>詳細設定 </p></td> 
  <td class="stentry"> <p>OPI コメントを保持は常にオンになっています。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>規格 </p></td> 
  <td class="stentry"> <p>コンプライアンス基準。 </p></td> 
 </tr> 
</table>
