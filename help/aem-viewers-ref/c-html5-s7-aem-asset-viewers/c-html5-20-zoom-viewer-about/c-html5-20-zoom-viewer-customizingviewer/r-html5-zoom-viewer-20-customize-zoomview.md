---
title: ズームビュー
description: メインビューは、ズーム可能な画像で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
TQID: 'https://experienceleague.adobe.com/i1B2r5g74xmk6H3DLD12gyRI9uJo32p3SmgS-OFnLf8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# ズームビュー{#zoom-view}

メインビューは、ズーム可能な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

表示領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> メインビューの16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カーソル </span> </p> </td> 
   <td colname="col2"> <p>メインビューの上にカーソルが表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にします。

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`.s7zoomview` クラスに適用できる`cursortype`属性セレクターをサポートしています。 コンポーネントの状態とユーザーアクションに基づいてカーソルの種類を制御します。 次の`cursortype`値がサポートされています：

* `default`

  画像の解像度が小さい場合、またはコンポーネントの設定が原因で画像がズームできない場合、またはその両方が表示されます。

* `zoomin`

  画像をズームインできる場合に表示されます。

* `reset`

  画像が最大ズームレベルで、初期状態にリセットできる場合に表示されます。

* `drag`

  ユーザーがズームイン状態の画像をパンしたときに表示されます。

* `slide`

  ユーザーが水平方向のスワイプまたはフリックを行って画像の入れ替えを実行したときに表示されます。
