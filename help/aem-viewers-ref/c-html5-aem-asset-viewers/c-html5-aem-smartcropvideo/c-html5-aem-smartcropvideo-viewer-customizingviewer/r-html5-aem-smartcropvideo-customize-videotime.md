---
title: ビデオ時間
description: ビデオ時間は、現在再生中のビデオの現在の時間とデュレーションを示す数値表示です。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
TQID: 'https://experienceleague.adobe.com/Ln-FEgGu-vFMAL25NbhWYqoBm7NSN1waCeQE85xdxOk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%
---
# ビデオ時間{#video-time}

ビデオ時間は、現在再生中のビデオの現在の時間とデュレーションを示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオタイムのフォントファミリー、フォントサイズ、フォントカラーは、CSSで制御できるプロパティの1つです。 また、それを含むコントロールバーに対して、CSSで配置することもできます。

ビデオ時間のアピアランスは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7videotime
```

## ビデオタイムのCSS プロパティ {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む右端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> ビデオタイムコントロールの幅。 このプロパティは、Internet Explorer 8以降が正しく機能するために必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

ビデオ時間をライトグレー（12 ピクセルの大きさ`#BBBBBB`）に設定し、コントロールバーの上部から15 ピクセル、コントロールバーの右端から80 ピクセルに配置します。

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
