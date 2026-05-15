---
title: キーボードによるアクセシビリティとナビゲーション
description: Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Dimensional （3D）、Carousel、Interactive Image、Interactive Video、Video360 ビューアインターフェイスで表示されるすべての機能にキーボードからアクセスできます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
TQID: 'https://experienceleague.adobe.com/Yo1xl9U8Ld3nzbeHm6pQxAncRKQIXEWimijQM4FjLtc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 588
ht-degree: 0%

---

# キーボードによるアクセシビリティとナビゲーション{#keyboard-accessibility-and-navigation}

Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Carousel、Dimensional （3D）、Interactive Image、Interactive Video、Video360 ビューアインターフェイスで表示されるすべての機能にキーボードからアクセスできます。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## キーボードによるアクセシビリティとナビゲーション {#topic-f5650e9493404e55a3627c8d1366b861}

Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Carousel、Dimensional （3D）、Interactive Image、Interactive Video、Video360 ビューアインターフェイスで表示されるすべての機能にキーボードからアクセスできます。

エンドユーザーは、**[!UICONTROL Tab]**&#x200B;と&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;のキーストロークを使用して、ビューアーユーザーインターフェイス要素間を移動できます。 **[!UICONTROL Tab]**&#x200B;を使用すると、入力フォーカスがタブ順の次のユーザーインターフェイス要素に進みます。**[!UICONTROL Shift+Tab]**&#x200B;を使用すると、入力フォーカスが前のユーザーインターフェイス要素に戻ります。 フォーカストラバーサルは、画面上の自然なユーザーインターフェイス要素の位置に従い、左から右、次に上から下の順序で移動します。

オペレーティングシステムとweb ブラウザーの設定に応じて、入力フォーカスを持つユーザーインターフェイス要素は視覚的なフォーカス表示を受け取ります。 例えば、ビジュアルインジケーターは、ユーザーインターフェイス要素の周囲に表示される細い境界線です。

ビューア CSSでは、このようなフォーカスのハイライトを無効にしたり、カスタマイズしたりできます。 このヘルプシステムの目次で、特定のビューア名（基本ズームやインタラクティブビデオなど）の下で、**ビューアの&#x200B;*名前のカスタマイズ*** >** フォーカスハイライト **をクリックします。

個々のビューアのユーザーインターフェイス要素でサポートされているキーストロークは、ほとんどの場合、わかりやすく、見つけやすいものです。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アクション </p> </th> 
   <th colname="col2" class="entry"> <p>キーストローク </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ボタンコンポーネントをアクティベート </p> </td> 
   <td colname="col2"> <p>スペースまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームインまたはズームアウト </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span>または<span class="uicontrol"> - </span>をそれぞれ使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームリセット </p> </td> 
   <td colname="col2"> <p>Esc キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>パン </p> </td> 
   <td colname="col2"> <p>上、下、左、または右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>360度画像の回転 </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合は、矢印キーを使用します。 </p> <p>多次元スピンセットを操作する場合は、上向き矢印キーまたは下向き矢印キーを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチの選択 </p> </td> 
   <td colname="col2"> <p>上、下、左、または右向き矢印キー、ホーム キーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、段階的な巻き戻し </p> </td> 
   <td colname="col2"> <p>左向き矢印または上向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>動画とインタラクティブビデオを利用できます </p> </td> 
   <td colname="col2"> <p>右または下向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>動画とインタラクティブビデオ、先頭または末尾に移動 </p> </td> 
   <td colname="col2"> <p>Home キーまたはEnd キーをそれぞれ使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、フォーカスがスライダー上にある場合のボリュームレベルの制御 </p> </td> 
   <td colname="col2"> <p>上、下、左、または右向き矢印キー、ホーム キーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、可変ボリューム </p> </td> 
   <td colname="col2"> <p>スライダー部分にフォーカスがある場合にボリュームレベルを制御する矢印、ホーム、終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオでは、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールのみに制限されます。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、メインビューでのバナー画像の変更 </p> </td> 
   <td colname="col2"> <p>左向き矢印または右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、ホットスポットの選択、ホットスポットのアクティベーション </p> </td> 
   <td colname="col2"> <p>ホットスポットの選択：上、下、左、または右矢印キー </p> <p>ホットスポットのアクティベーション：スペースまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalogの場合、メインビューでページ画像を変更します </p> </td> 
   <td colname="col2"> <p> 左右の矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、サムネール選択 </p> </td> 
   <td colname="col2"> <p>矢印キー、ホーム キーと終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ホットスポット選択 </p> </td> 
   <td colname="col2"> <p>矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e カタログ、アクティベーション </p> </td> 
   <td colname="col2"> <p>スペース キーまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ドロップダウンコンポーネントのアクティブ化 </p> </td> 
   <td colname="col2"> <p> 下向き矢印キー、スペースまたはEnter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、フォーカスがドロップダウンパネルにある場合 </p> </td> 
   <td colname="col2"> <p>矢印キーを使用して、パネル内の特定の項目を選択してからアクティブ化します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalogでは、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールのみに制限されます。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
