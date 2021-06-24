---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> ページ画像に適用される画像サービングコマンド文字列。 URLで指定する場合、 <span class="codeph"> &amp;</span>と<span class="codeph"> =</span>はすべて、 <span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードする必要があります。 </p> <p> <p>注意： 画像のサイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-df5a0604766b4ac2b9a6742b377e427c}

（オプション）

## 初期設定 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

なし

## 例 {#section-813de2905d6c44c0991cfe0931581462}

ビューアのURLで指定する場合。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

configデータで指定する場合。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
