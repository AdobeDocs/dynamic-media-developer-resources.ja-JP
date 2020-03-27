---
description: インタラクティブビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージが含まれます。
seo-description: インタラクティブビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージが含まれます。
seo-title: ユーザーインターフェイス要素のローカリゼーション
solution: Experience Manager
title: ユーザーインターフェイス要素のローカリゼーション
topic: Dynamic media
uuid: 7c880e25-76dc-43d3-83fc-12de92afd35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

インタラクティブビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 任意のシンボルには、標準搭載のビューアに付属する英語のロケール( `"en"`)に対する初期設定の関連テキスト値が含まれ、また、必要な数のロケールに対してユーザ定義の値が設定される場合があります。

ビューアを起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義値が存在するかどうかが確認されます。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカリゼーションデータは、ローカリゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケール、各ロケールのシンボルテキスト値、およびデフォルトロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

上の例では、ローカリゼーションオブジェクトは2つのロケール(および `"en"` )を定義し、 `"fr"`各ロケールの2つのユーザーインターフェイス要素のローカリゼーションを提供します。

Webページコードは、設定オブジェクトのフィールドの値として、ローカリゼーションオブジェクトをビューアのコ `localizedTexts` ンストラクターに渡す必要があります。 別の方法として、メソッドを呼び出してローカリゼーションオブジェクトを渡す方法が `setLocalizedTexts(localizationInfo)` あります。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>ツールチップの対象 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIAの最上位ビューア要素のラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止ボタンが選択された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンが選択解除された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止ボタンの状態を再生 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> ミュート可能ボリュームを選択 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームの選択を解除 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> ARIA aria-valuetextアトリビュートを使用して公開されるボリュームス <span class="codeph"> ライダのノブのラ </span> ベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>通常の状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションボタンが選択された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションボタンが選択解除された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER </span> </p> </td> 
   <td colname="col2"> <p>バナーのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>上スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>下スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>リンク共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスの右上の閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>共有リンクの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>キャンセルボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> 「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebookの共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Twitterの共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>誘い文句（CTA：コールトゥアクション）パネルの閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>再生可能なビデオがない場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

