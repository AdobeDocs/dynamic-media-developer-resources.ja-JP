---
description: ビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。
seo-description: ビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。
seo-title: ユーザーインターフェイス要素のローカリゼーション
solution: Experience Manager
title: ユーザーインターフェイス要素のローカリゼーション
topic: Dynamic media
uuid: 05b88ef9-0d90-4143-8558-d0d32943c348
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

ビデオビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 任意のシンボルには、標準搭載のビューアに付属の英語ロケール( `"en"`)の初期設定の関連テキスト値があります。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアを起動すると、現在のロケールがチェックされ、ロケールでサポートされている各シンボルに対してユーザ定義の値が存在するかどうかが確認されます。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

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

上の例では、ローカリゼーションオブジェクトは2つのロケール（および）を定義し、 `"en"` 各ロケールの2つ `"fr"`のユーザーインターフェイス要素のローカリゼーションを提供します。

Webページコードは、設定オブジェクトのフィールドの値として、このようなローカリゼーションオブジェクトをビューアのコ `localizedTexts` ンストラクターに渡す必要があります。 別の方法として、メソッドを呼び出してローカリゼーションオブジェクトを渡す方法があ `setLocalizedTexts(localizationInfo)` ります。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> ARIAの最上位ビューア要素のラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンが選択された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンが選択解除された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームが選択された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームの選択を解除した場合のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> ARIA aria-valuetextアトリビュートを使用して公開されるボリュームス <span class="codeph"> ライダのノブのラ </span> ベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンが選択された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンが選択解除された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションボタンが選択された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションボタンが選択解除された状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>電子メール共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>電子メールダイアログヘッダーのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>電子メールダイアログボックスの右上の閉じるボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS </span> </p> </td> 
   <td colname="col2"> <p>電子メールアドレスの形式が正しくない場合に表示されるエラーメッセージのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>「宛先」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>「別の電子メールアドレスを追加」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>「別の電子メールアドレスを追加」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>「送信者」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>「メッセージ」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>「電子メールアドレスを削除」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>フォームの送信後にダイアログの下部に表示される閉じるボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>フォームの送信後にダイアログの下部に表示される閉じるボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>電子メールが正常に送信された場合に表示される確認メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>電子メールが正常に送信されなかった場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>埋め込み共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスのヘッダーのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスの右上の閉じるボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードテキストの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックスのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックスの最後の「カスタムサイズ」エントリのテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>リンク共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスのヘッダーのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスの右上の閉じるボタンのツールチップ。 </p> </td> 
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
   <td colname="col2"> <p>「キャンセル」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Twitter共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>再生可能なビデオがない場合に表示されるエラーメッセージのツールチップ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

