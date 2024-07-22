---
title: ユーザーインターフェイス要素のローカリゼーション
description: 混在メディアビューアに表示される特定のコンテンツは、ローカライゼーションの対象となります。 このガイドラインには、ズームボタン、スピンボタン、ビデオコントロール、クローズボタン、フルスクリーンボタンおよびスウォッチスクロールボタンが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 119d8dde-145b-4762-a1ab-882a29e0f6a6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

混在メディアビューアに表示される特定のコンテンツは、ローカライゼーションの対象となります。 このガイドラインには、ズームボタン、スピンボタン、ビデオコントロール、クローズボタン、フルスクリーンボタンおよびスウォッチスクロールボタンが含まれます。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOL と呼ばれる特別な Viewer SDK 識別子で表されます。 すべての SYMBOL には、デフォルトのビューアに付属する英語ロケール（`"en"`）のテキスト値が関連付けられています。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアは起動時、現在のロケールを調べて、そのロケールでサポートされている各 SYMBOL にユーザー定義の値があるかどうかを確認します。 デフォルト値が存在する場合は、ユーザー定義の値が使用され、存在しない場合は、標準のデフォルトテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケール、各ロケールの SYMBOL テキスト値、デフォルトのロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

上記の例では、localization オブジェクトは 2 つのロケール（`"en"` と `"fr"`）を定義し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページのコードは、ローカリゼーションオブジェクトを、設定オブジェクトの `localizedTexts` フィールドの値としてビューアのコンストラクターに渡す必要があります。 別のオプションとして、`setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカリゼーションオブジェクトを渡すこともできます。

次の記号がサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>記号 </p> </th> 
   <th colname="col2" class="entry"> <p>ツールヒント： </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>最上位のビューア要素の ARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ZoomView.ROLE_DESCRIPTION </span> を <span class="codeph"> きます。 </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA 役割の説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザー向けの ARIA 使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA 役割の説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザー向けの ARIA 使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA 役割の説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザー向けの ARIA 使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「閉じる」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「ズームイン」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームアウトボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームリセットボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>インライン </span> ールズームモード <span class="codeph"> デスクトップシステム。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>インラインタッチズームモード <span class="codeph"> デバイ </span> をタッチします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全画面表示ボタンが通常の状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した字幕ボタンの状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションボタンの状態が選択されていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>左ボタンをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>右にスクロール ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スクロールアップボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スクロールダウンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スピン左ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スピン右ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生の一時停止ボタンの状態を選択しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生の一時停止ボタンの状態の選択が解除されました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>一時停止ボタンの状態を再生します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>可変ボリューム状態を選択しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>可変ボリュームの選択が解除されました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p>ARIA <span class="codeph"> aria-valuetext </span> 属性を介して公開されるボリュームスライダーノブのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>ビデオを再生できないときに表示されるエラーメッセージ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
