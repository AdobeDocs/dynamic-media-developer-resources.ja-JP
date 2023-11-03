---
title: ユーザーインターフェイス要素のローカライゼーション
description: ビデオビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザーインターフェイス要素のツールチップや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 4748d04e-7f9d-413f-9e9a-a0fad129c5fc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

ビデオビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザーインターフェイス要素のツールチップや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。

ビューア内のテキスト内のローカライズ可能なコンテンツは、SYMBOL と呼ばれる、特別な Viewer SDK 識別子で表されます。 SYMBOL には、英語のロケール ( `"en"`) には、標準のビューアが付属しています。 また、必要な数のロケールに対して、ユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされる各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値を使用します。それ以外の場合は、標準のデフォルトテキストにフォールバックされます。

ユーザ定義のローカリゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケール、各ロケールの SYMBOL テキスト値、およびデフォルトのロケールのリストが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

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

上記の例では、ローカリゼーションオブジェクトで 2 つのロケール ( `"en"` および `"fr"`) を参照し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページコードでは、このようなローカリゼーションオブジェクトをの値としてビューアのコンストラクターに渡す必要があります。 `localizedTexts` 設定オブジェクトのフィールド。 別のオプションとして、 `setLocalizedTexts(localizationInfo)` メソッド。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>記号 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> トップレベルのビューア要素の ARIA ラベル。 </p> </td> 
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
   <td colname="col2"> <p>再生/一時停止ボタンの状態に関するツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した可変ボリュームの状態のツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームを選択解除するためのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> ARIA を介して公開されるボリュームスライダーノブラベル <span class="codeph"> aria-valuetext </span> 属性。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSSS </span> </p> </td> 
   <td colname="col2"> <p>E メールアドレスの形式が正しくない場合に表示されるエラーメッセージのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>「宛先」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>「別のメールアドレスを追加」ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>「別のメールアドレスを追加」ボタンのキャプション。 </p> </td> 
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
   <td colname="col2"> <p>「メールアドレスを削除」ボタンのツールチップ。 </p> </td> 
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
   <td colname="col2"> <p>電子メールが正常に送信された際に表示される確認メッセージ。 </p> </td> 
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
   <td colname="col2"> <p>埋め込みダイアログボックスヘッダーのツールチップ。 </p> </td> 
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
   <td colname="col2"> <p>[ すべて選択 ] ボタンのツールチップ。 </p> </td> 
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
   <td colname="col2"> <p>リンクダイアログボックスヘッダーのツールチップ。 </p> </td> 
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
   <td colname="col2"> <p>[ すべて選択 ] ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「Facebook」共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>twitter共有ボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>ビデオの再生が不可能な場合に表示されるエラーメッセージのツールチップ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
