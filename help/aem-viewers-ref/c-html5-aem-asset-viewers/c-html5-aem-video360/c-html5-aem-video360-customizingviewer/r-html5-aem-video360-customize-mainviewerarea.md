---
description: メイン表示領域は、360ビデオが表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Mediaクラシック，ビューア，SDK/API,360 VRビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# メインビューア領域{#main-viewer-area}

メイン表示領域は、360ビデオが表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7video360viewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-ee18025b182a42dc98052de5f133ddfe}

白の背景(`#FFFFFF`)のビューアを設定し、サイズを512 x 288ピクセルにするには、次のように記述します。

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

