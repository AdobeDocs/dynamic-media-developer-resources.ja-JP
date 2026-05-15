---
title: ビデオプレーヤー
description: ビデオプレーヤーは、ビデオコンテンツがビューア内に表示される長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
TQID: 'https://experienceleague.adobe.com/ZpzG5EIBnwZkkj9-feZEOynAP8viF-mx8XFi8OKzI-o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 290
ht-degree: 0%

---

# ビデオプレーヤー{#video-player}

ビデオプレーヤーは、ビデオコンテンツがビューア内に表示される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生されるビデオのサイズがビデオプレーヤーのサイズと一致しない場合、ビデオコンテンツはビデオプレーヤーの長方形表示領域内に配置されます。

次のCSS クラスセレクターは、ビデオプレーヤーの外観を制御します。

```
.s7mixedmediaviewer .s7videoplayer
```

ビデオプレーヤーの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> ビデオプレーヤーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

システムがビデオを再生できない場合に表示されるエラーメッセージは、ローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

例 – ビデオプレーヤーを透明にするには：

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

キャプションはビデオプレーヤー内の内部コンテナに入れられます。 そのコンテナの位置は、サポートされているWebVTT ポジショニングオペレーターによって制御されます。 キャプションテキスト自体はそのコンテナ内にあります。そのスタイルは、次のCSS クラスセレクターで制御されます。

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**キャプションのCSS プロパティ**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>キャプションテキストの背景： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>キャプションテキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 半透明の黒い背景にキャプションテキストを14 ピクセルの薄いグレーのArial®に設定するには、次の手順を実行します。

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

バッファリングアニメーションの外観は、次のCSS クラスセレクターで制御されます。

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
```

待機アイコン **の** CSS プロパティ

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの左余白。通常は、アイコンの幅の半分を引きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの上余白（通常はアイコンの高さの半分を差し引く）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> ノブのアートワーク： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – バッファリングアニメーションを幅101 ピクセル、高さ29 ピクセルに設定するには、次の手順を実行します。

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
