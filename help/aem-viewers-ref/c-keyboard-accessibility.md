---
title: キーボードのアクセシビリティとナビゲーション
description: 基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、ディメンショナル (3D)、カルーセル、インタラクティブ画像、インタラクティブビデオ、Video360 の各ビューアインターフェイスで公開されているすべての機能にキーボードアクセスできます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# キーボードのアクセシビリティとナビゲーション{#keyboard-accessibility-and-navigation}

基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、ディメンショナル (3D)、インタラクティブ画像、インタラクティブビデオ、ビデオ 360 の各ビューアインターフェイスで公開されているすべての機能にキーボードアクセスできます。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## キーボードのアクセシビリティとナビゲーション {#topic-f5650e9493404e55a3627c8d1366b861}

基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、ディメンショナル (3D)、インタラクティブ画像、インタラクティブビデオ、ビデオ 360 の各ビューアインターフェイスで公開されているすべての機能にキーボードアクセスできます。

エンドユーザーは、 **[!UICONTROL タブ]** および **[!UICONTROL Shift+Tab]** キー操作 使用 **[!UICONTROL タブ]** 入力フォーカスをタブ順序内の次のユーザーインターフェイス要素に進めます。using **[!UICONTROL Shift+Tab]** 前のユーザーインターフェイス要素に入力フォーカスを戻します。 フォーカストラバーサルは、画面上の自然なユーザーインターフェイス要素の位置に従って、左から右、上から下の順に移動します。

オペレーティングシステムと Web ブラウザーの設定に応じて、入力フォーカスを持つユーザーインターフェイス要素が視覚的なフォーカス表示を受け取ります。 例えば、視覚的インジケーターは、ユーザーインターフェイス要素の周りにレンダリングされる細い境界線にすることができます。

ビューアの CSS で、このようなフォーカスハイライトを無効にしたりカスタマイズしたりできます。 このヘルプシステムの目次で、特定のビューア名（基本ズーム、インタラクティブビデオなど）の下で、 **カスタマイズ *ビューア名*** >**&#x200B;フォーカスのハイライト&#x200B;**.

個々のビューアのユーザインターフェイス要素でサポートされるキーストロークは、ほとんどの場合、明らかで見つけやすいものです。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アクション </p> </th> 
   <th colname="col2" class="entry"> <p>キー操作 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ボタンコンポーネントをアクティブ化 </p> </td> 
   <td colname="col2"> <p>スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームインまたはズームアウト </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> または <span class="uicontrol"> - </span>、それぞれ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームのリセット </p> </td> 
   <td colname="col2"> <p>Esc キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>パン </p> </td> 
   <td colname="col2"> <p>上、下、左、右の矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>360 度の画像の回転 </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合は、矢印キーを使用します。 </p> <p>複数次元のスピンセットを操作する場合は、上向き矢印キーまたは下向き矢印キーを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチの選択 </p> </td> 
   <td colname="col2"> <p>上、下、左、右の矢印キー。ホームキーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオおよびインタラクティブビデオ、徐々に巻き戻す </p> </td> 
   <td colname="col2"> <p>左向き矢印キーまたは上向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオおよびインタラクティブビデオ、早送り </p> </td> 
   <td colname="col2"> <p>右向き矢印キーまたは下向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオおよびインタラクティブビデオ、開始または終了 </p> </td> 
   <td colname="col2"> <p>ホームキーと終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、フォーカスがスライダーにあるときの音量レベルを制御 </p> </td> 
   <td colname="col2"> <p>上、下、左、右の矢印キー。ホームキーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、可変ボリューム </p> </td> 
   <td colname="col2"> <p>フォーカスがスライダパーツにあるときにボリュームレベルを制御する矢印キー、ホームキー、終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオでは、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールにのみ制限されます。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、メインビューのバナー画像を変更 </p> </td> 
   <td colname="col2"> <p>左向き矢印キーまたは右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、ホットスポット選択、ホットスポットのアクティベーション </p> </td> 
   <td colname="col2"> <p>ホットスポットの選択：上、下、左、右矢印キー </p> <p>ホットスポットのアクティベーション：スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog で、メインビューのページ画像を変更します。 </p> </td> 
   <td colname="col2"> <p> 左右の矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、サムネールの選択 </p> </td> 
   <td colname="col2"> <p>矢印キー；ホームキーとエンドキー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ホットスポット選択 </p> </td> 
   <td colname="col2"> <p>矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、アクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ドロップダウンコンポーネントのアクティブ化 </p> </td> 
   <td colname="col2"> <p> 下向き矢印キー；スペース、または Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog（フォーカスがドロップダウンパネルにある場合） </p> </td> 
   <td colname="col2"> <p>アクティブ化する前に、矢印キーを使用して、パネル内の特定の項目を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog では、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールにのみ制限されます。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
