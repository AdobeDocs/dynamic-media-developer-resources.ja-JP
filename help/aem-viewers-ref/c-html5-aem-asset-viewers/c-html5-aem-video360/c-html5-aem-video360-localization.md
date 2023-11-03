---
title: ユーザーインターフェイス要素のローカライゼーション
description: 閲覧者が表示するコンテンツには、ローカライゼーションの対象となるものもあります。 このようなコンテンツには、ユーザーインターフェイス要素のツールチップや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: d54fd841-2246-4d2e-8bf9-7da56f2487f3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

閲覧者が表示するコンテンツには、ローカライゼーションの対象となるものもあります。 このようなコンテンツには、ユーザーインターフェイス要素のツールチップや、ビデオを再生できない場合に表示されるエラーメッセージなどが含まれます。

ビューア内のテキスト内のローカライズ可能なコンテンツは、SYMBOL と呼ばれる、特別な Viewer SDK 識別子で表されます。 SYMBOL には、英語のロケール ( `"en"`) には、標準のビューアが付属しています。 また、必要な数のロケールに対して、ユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされる各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値を使用します。それ以外の場合は、標準のデフォルトテキストにフォールバックされます。

ユーザ定義のローカリゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケール、各ロケールの SYMBOL テキスト値、およびデフォルトのロケールのリストが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

上記の例では、ローカリゼーションオブジェクトで 2 つのロケール ( `"en"` および `"fr"`) を参照し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページコードでは、ローカリゼーションオブジェクトを `localizedTexts` 設定オブジェクトのフィールド。 別のオプションとして、 `setLocalizedTexts(localizationInfo)` メソッド。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>記号 </p> </th> 
   <th colname="col2" class="entry"> <p>ツールチップの表示… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>トップレベルのビューア要素の ARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態が選択されました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンが選択解除された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選択した可変ボリュームの状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームの選択を解除。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p>ARIA を介して公開されるボリュームスライダーノブラベル <span class="codeph"> aria-valuetext </span> 属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタン（通常の状態） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>埋め込み共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスの右上にある閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックスの最後の「カスタムサイズ」エントリ。 </p> </td> 
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
   <td colname="col2"> <p>共有リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP ACTION </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「 Facebook 」共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>twitter共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Video360Player.ERROR </span> </p> </td> 
   <td colname="col2"> <p>再生可能なビデオがない場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
