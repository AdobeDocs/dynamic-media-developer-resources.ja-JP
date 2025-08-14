---
title: ユーザーインターフェイス要素のローカリゼーション
description: スマート切り抜きビデオビューアに表示される特定のコンテンツは、ローカライゼーションの影響を受けます。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、ビデオを再生できない場合に表示されるエラーメッセージが含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e5019948-d8ed-4bb2-b652-2936b6f694c9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

スマート切り抜きビデオビューアに表示される特定のコンテンツは、ローカライゼーションの影響を受けます。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、ビデオを再生できない場合に表示されるエラーメッセージが含まれています。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOL と呼ばれる特別なビューアSDK識別子で表されます。 すべての SYMBOL には、デフォルトのビューアに付属する英語ロケール（`"en"`）のテキスト値が関連付けられています。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアは起動時、現在のロケールを調べて、そのロケールでサポートされている各 SYMBOL にユーザー定義の値があるかどうかを確認します。 デフォルト値が存在する場合は、ユーザー定義の値が使用され、存在しない場合は、標準のデフォルトテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケール、各ロケールの SYMBOL テキスト値、デフォルトのロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

上記の例では、localization オブジェクトは 2 つのロケール（`"en"` と `"fr"`）を定義し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページのコードは、このようなローカリゼーションオブジェクトを、設定オブジェクトのフィールドの値としてビューアのコンストラクター `localizedTexts` 渡す必要があります。 別のオプションとして、`setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカリゼーションオブジェクトを渡すこともできます。

次の記号がサポートされています。

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
   <td colname="col2"> <p> 最上位のビューア要素の ARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した再生一時停止ボタン状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択解除された再生の一時停止ボタンの状態に関するツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>再生の一時停止ボタン状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間用のツールヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した可変ボリューム状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択解除された可変ボリュームのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> ARIA <span class="codeph"> aria-valuetext </span> 属性を介して公開されるボリュームスライダーノブのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した全画面表示ボタンの状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択解除されたフルスクリーンボタン状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択したクローズドキャプションボタンの状態のツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>非選択のクローズドキャプションボタンの状態に関するツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「メール共有」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>メールダイアログヘッダーのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>メールダイアログボックスの右上の「閉じる」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSES </span> </p> </td> 
   <td colname="col2"> <p>メールアドレスの形式が正しくない場合に表示されるエラーメッセージのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>「宛先」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>「別のメールアドレスを追加」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>「別のメールアドレスを追加」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>「送信元」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>「メッセージ」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>「メールアドレスを削除」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>[ キャンセル ] ボタンのキャプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>フォームの送信後にダイアログの下部に表示される閉じるボタンのキャプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信後にダイアログの下部に表示される「閉じる」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>メールが正常に送信されたときに表示される確認メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>メールが正常に送信されなかった場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> EmbedShare.TOOLTIP <span class="codeph"> を </span> します </p> </td> 
   <td colname="col2"> <p>「埋め込み共有」ボタンのツールヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.HEADER </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスヘッダーのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスの右上の「閉じる」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードテキストの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズ コンボボックスのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>[ キャンセル ] ボタンのキャプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> EmbedShare.ACTION <span class="codeph"> を </span> します </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP アクション </span> </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> EmbedShare.CUSTOM_SIZE <span class="codeph"> を </span> します </p> </td> 
   <td colname="col2"> <p>埋め込みサイズ コンボボックスの最後の「カスタムサイズ」エントリのテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>リンク共有ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.HEADER </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスのヘッダーのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスの右上の「閉じる」ボタンのツールヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>共有リンクの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>[ キャンセル ] ボタンのキャプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> LinkShare.TOOLTIP アクション <span class="codeph"> を </span> します </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook 共有ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> TwitterShare.TOOLTIP <span class="codeph"> を </span> きます </p> </td> 
   <td colname="col2"> <p>「Twitter 共有」ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SmartCropVideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>ビデオを再生できないときに表示されるエラーメッセージのツールヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
