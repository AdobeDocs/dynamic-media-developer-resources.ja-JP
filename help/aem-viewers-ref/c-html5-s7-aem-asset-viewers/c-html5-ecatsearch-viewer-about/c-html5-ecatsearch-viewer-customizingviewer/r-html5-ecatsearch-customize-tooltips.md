---
title: ツールヒント
description: デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素には、マウスポインターに表示されるツールヒントがあります。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0350bdbc-3e3d-4bc0-98f6-5d7bf4121d9a
TQID: 'https://experienceleague.adobe.com/xbY-qgovrPdEqCBWX0YG5OnZJL2FiVxvRnZWca0r1EU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# ツールヒント{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素には、マウスポインターに表示されるツールヒントがあります。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

ツールヒントの表示は、次のCSS クラスセレクターで制御します。

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
>ツール ヒントのスタイルが埋め込みweb ページ内からカスタマイズされる場合、すべてのプロパティに`!IMPORTANT` ルールを含める必要があります。 ツールヒントがビューアのCSS ファイルでカスタマイズされている場合、このルールは必要ありません。

例 – Arial®で書かれた3 pxのコーナー半径、黒い背景、白いテキストを含むグレーの境界線を持つツールヒントを設定するには、次の手順を実行します。

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
