---
title: キーボードのアクセシビリティとナビゲーション
description: 基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、ディメンション（3D）、カルーセル、インタラクティブ画像、インタラクティブビデオ、ビデオ 360 ビューアインターフェイスで公開されるすべての機能には、キーボードでアクセスできます。
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

基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、ディメンション（3D）、インタラクティブ画像、インタラクティブビデオ、ビデオ 360 ビューアインターフェイスで公開されるすべての機能には、キーボードでアクセスできます。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## キーボードのアクセシビリティとナビゲーション {#topic-f5650e9493404e55a3627c8d1366b861}

基本ズーム、eCatalog、eCatalog 検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、ディメンション（3D）、インタラクティブ画像、インタラクティブビデオ、ビデオ 360 ビューアインターフェイスで公開されるすべての機能には、キーボードでアクセスできます。

エンドユーザーは、**[!UICONTROL Tab]** キーと **[!UICONTROL Shift+Tab]** キーを使用して、ビューアのユーザーインターフェイス要素間を移動できます。 **[!UICONTROL Tab]** キーを使用すると、入力フォーカスがタブ順に次のユーザーインターフェイス要素に移動します。**[!UICONTROL Shift+Tab]** キーを使用すると、入力フォーカスが前のユーザーインターフェイス要素に戻ります。 フォーカスのトラバーサルは、画面上の自然なユーザーインターフェイス要素の位置を追い、左から右、上から下の順に移動します。

オペレーティングシステムと web ブラウザーの設定に応じて、入力フォーカスのあるユーザーインターフェイス要素に視覚的なフォーカス表示が送られます。 例えば、視覚的なインジケーターは、ユーザーインターフェイス要素の周囲にレンダリングされる薄い境界線にすることができます。

ビューア CSS では、このようなフォーカスハイライト表示を無効にしたりカスタマイズしたりできます。 このヘルプ システムの目次で、特定のビューア名（基本ズーム、インタラクティブ ビデオなど）の下で、**カスタマイズ *ビューア名***>**&#x200B; フォーカス ハイライト &#x200B;** をクリックします。

個々のビューアのユーザーインターフェイス要素でサポートされているキーストロークは、ほとんどの場合、明確で見つけやすくなっています。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アクション </p> </th> 
   <th colname="col2" class="entry"> <p>キーストローク </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ボタンコンポーネントのアクティベート </p> </td> 
   <td colname="col2"> <p>スペースまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームイン/ズームアウト </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> または <span class="uicontrol"> - </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームのリセット </p> </td> 
   <td colname="col2"> <p>Esc キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>パン </p> </td> 
   <td colname="col2"> <p>上向き、下向き、左向きまたは右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>360 度の画像のスピン </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合は、矢印キーを使用します。 </p> <p>多次元スピンセットを操作する場合は、上向き矢印キーまたは下向き矢印キーを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチの選択 </p> </td> 
   <td colname="col2"> <p>上向き、下向き、左向き、右向きの矢印キー。Home または End キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、徐々に巻き戻し </p> </td> 
   <td colname="col2"> <p>左向き矢印キーまたは上向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、早送り </p> </td> 
   <td colname="col2"> <p>右矢印キーまたは下矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオおよびインタラクティブビデオ。最初または最後に移動 </p> </td> 
   <td colname="col2"> <p>Home キーまたは End キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ（フォーカスがスライダーにあるときのボリュームレベルを制御） </p> </td> 
   <td colname="col2"> <p>上向き、下向き、左向き、右向きの矢印キー。Home または End キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、可変ボリューム </p> </td> 
   <td colname="col2"> <p>矢印キー、ホームキー、終了キーを使用して、スライダー部分にフォーカスを合わせたときのボリュームレベルを制御します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオでは、モーダルダイアログボックスが表示されると、フォーカスの移動がダイアログボックスのコントロールのみに制限されます。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、メインビューでのバナー画像の変更 </p> </td> 
   <td colname="col2"> <p>左向き矢印または右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、ホットスポットの選択、ホットスポットのアクティブ化 </p> </td> 
   <td colname="col2"> <p>ホットスポットの選択：上向き、下向き、左向き、右向き矢印キー </p> <p>ホットスポットアクティベーション：スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog のメインビューでのページ画像の変更 </p> </td> 
   <td colname="col2"> <p> 左矢印キーまたは右矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、サムネール選択 </p> </td> 
   <td colname="col2"> <p>矢印キー、Home キーと End キー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ホットスポットの選択 </p> </td> 
   <td colname="col2"> <p>矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, アクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, ドロップダウン コンポーネントのアクティブ化 </p> </td> 
   <td colname="col2"> <p> 下矢印キー、スペースまたは Enter キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog （フォーカスがドロップダウンパネルにあるとき） </p> </td> 
   <td colname="col2"> <p>矢印キーを使用して、パネル内の特定の項目を選択してからアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog では、モーダルダイアログボックスが表示されると、フォーカスの走査がダイアログボックスのコントロールのみに制限される。 </p> </td> 
   <td colname="col2"> <p>Esc キーを押してダイアログボックスを閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
