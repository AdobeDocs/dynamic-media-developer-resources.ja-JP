---
description: 基本ズーム、eCatalog、eCatalog検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、ディメンショナル(3D)、カルーセル、インタラクティブ画像、インタラクティブビデオ、ビデオ360の各ビューアインターフェイスで公開されている機能は、キーボード操作可能です。
solution: Experience Manager
title: キーボードのアクセシビリティとナビゲーション
feature: Dynamic Media Classic，ビューア，SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# キーボードのアクセシビリティとナビゲーション{#keyboard-accessibility-and-navigation}

基本ズーム、eCatalog、eCatalog検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、寸法(3D)、インタラクティブ画像、インタラクティブビデオ、ビデオ360の各ビューアインターフェイスで公開されているすべての機能がキーボード操作可能です。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## キーボードのアクセシビリティとナビゲーション {#topic-f5650e9493404e55a3627c8d1366b861}

基本ズーム、eCatalog、eCatalog検索、フライアウト、インラインズーム、混在メディア、スピン、ビデオ、ズーム、カルーセル、寸法(3D)、インタラクティブ画像、インタラクティブビデオ、ビデオ360の各ビューアインターフェイスで公開されているすべての機能がキーボード操作可能です。

エンドユーザーは、**[!UICONTROL Tab]**&#x200B;キーストロークと&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;キーストロークを使用して、ビューアのユーザインターフェイス要素間を移動できます。 **[!UICONTROL Tab]**&#x200B;を使用すると、入力フォーカスがタブ順序内の次のユーザーインターフェイス要素に進みます。**[!UICONTROL Shift+Tab]**&#x200B;を使用すると、前のユーザーインターフェイス要素に入力フォーカスが戻ります。 フォーカストラバーサルは、画面上の自然なユーザーインターフェイス要素の位置に従って、左から右、上から下の順に移動します。

オペレーティングシステムとWebブラウザの設定に応じて、入力フォーカスを持つユーザインターフェイス要素が視覚的なフォーカス表示を受け取る。 例えば、視覚インジケーターは、ユーザーインターフェイス要素の周囲にレンダリングされる細い境界線にすることができます。

ビューアのCSSでは、このようなフォーカスハイライトを無効にしたり、カスタマイズしたりできます。 このヘルプシステムの目次で、特定のビューア名（基本ズームやインタラクティブビデオなど）の下の「**カスタマイズ&#x200B;*ビューア名*** /**&#x200B;フォーカスハイライト&#x200B;**」をクリックします。

個々のビューアのユーザインターフェイス要素でサポートされるキーストロークは、ほとんどの場合、明らかで見つけやすいものです。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アクション </p> </th> 
   <th colname="col2" class="entry"> <p>キー入力 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ボタンコンポーネントのアクティブ化 </p> </td> 
   <td colname="col2"> <p>スペースキーまたはEnterキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームインまたはズームアウト </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> +ま </span> たは <span class="uicontrol"> -  </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ズームリセット </p> </td> 
   <td colname="col2"> <p>Escキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>パン </p> </td> 
   <td colname="col2"> <p>上、下、左、右の矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>360度画像の回転 </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合は、矢印キーを使用します。 </p> <p>複数次元のスピンセットを操作する場合は、上向き矢印キーまたは下向き矢印キーを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチの選択 </p> </td> 
   <td colname="col2"> <p>上、下、左または右の矢印キー。ホームキーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>製品スウォッチのアクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたはEnterキー。 </p> </td> 
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
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、開始または終了 </p> </td> 
   <td colname="col2"> <p>HomeキーまたはEndキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ。フォーカスがスライダーにあるときの音量レベルを制御 </p> </td> 
   <td colname="col2"> <p>上、下、左または右の矢印キー。ホームキーまたは終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオとインタラクティブビデオ、可変ボリューム </p> </td> 
   <td colname="col2"> <p>フォーカスがスライダパーツにあるときのボリュームレベルを制御する矢印キー、ホームキー、終了キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビデオでは、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールのみに制限されます。 </p> </td> 
   <td colname="col2"> <p>Escキーを押して、ダイアログボックスを閉じます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、メインビューのバナー画像の変更 </p> </td> 
   <td colname="col2"> <p>左または右向き矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カルーセル、ホットスポット選択、ホットスポットのアクティブ化 </p> </td> 
   <td colname="col2"> <p>ホットスポットの選択：上、下、左または右向き矢印キー </p> <p>ホットスポットのアクティベート：スペースキーまたはEnterキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalogで、メインビューのページ画像を変更します。 </p> </td> 
   <td colname="col2"> <p> 左右の矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、サムネールの選択 </p> </td> 
   <td colname="col2"> <p>矢印キー；ホームキーと終了キー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，スウォッチのアクティブ化 </p> </td> 
   <td colname="col2"> <p>スペースキーまたはEnterキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ホットスポット選択 </p> </td> 
   <td colname="col2"> <p>矢印キー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、アクティベーション </p> </td> 
   <td colname="col2"> <p>スペースキーまたはEnterキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、ドロップダウンコンポーネントのアクティブ化 </p> </td> 
   <td colname="col2"> <p> 下向き矢印キースペース、またはEnterキー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog（フォーカスがドロップダウンパネルにある場合） </p> </td> 
   <td colname="col2"> <p>アクティブ化する前に、矢印キーを使用して、パネル内の特定の項目を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalogでは、モーダルダイアログボックスが表示されると、フォーカストラバーサルはダイアログボックスのコントロールのみに制限されます。 </p> </td> 
   <td colname="col2"> <p>Escキーを押して、ダイアログボックスを閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
