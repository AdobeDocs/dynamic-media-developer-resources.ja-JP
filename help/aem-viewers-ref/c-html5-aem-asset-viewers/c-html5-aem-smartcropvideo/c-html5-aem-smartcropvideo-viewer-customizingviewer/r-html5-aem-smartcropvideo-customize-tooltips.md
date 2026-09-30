---
title: ツールヒント
description: デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素には、マウスのカーソルを合わせるとツールヒントが表示されます。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 78cc0f11-bec2-495e-b3c9-a91b6bd1b1f0
TQID: 'https://experienceleague.adobe.com/UR-R8odmD4y-yLaJcb-MA0yLsnPq8KxRMOR0ImeU2fw'
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
source-wordcount: '144'
ht-degree: 0%
---
# ツールヒント{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素には、マウスのカーソルを合わせるとツールヒントが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

ツールヒントのアピアランスは、次のCSS クラスセレクターで制御されます。

```
.s7tooltip
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 背景色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>テキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>テキストフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントサイズ： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>ツールチップのスタイルが埋め込みweb ページ内からカスタマイズされる場合、すべてのプロパティに`!IMPORTANT` ルールを含める必要があります。 ツールヒントがビューアのCSS ファイルでカスタマイズされている場合、このルールは必要ありません。

例 – Arial®で書かれた3 pxのコーナー半径、黒い背景、白いテキストを含むグレーの境界線を持つツールチップを設定するには、次の手順を実行します。

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
