---
title: ユーザーインターフェイス要素のローカリゼーション
description: ビューアが表示する特定のコンテンツは、ローカライゼーションの対象となります。 このようなコンテンツには、ユーザーインターフェイス要素のツールチップと、ビデオを再生できないときに表示されるエラーメッセージが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: d54fd841-2246-4d2e-8bf9-7da56f2487f3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

ビューアが表示する特定のコンテンツは、ローカライゼーションの対象となります。 このようなコンテンツには、ユーザーインターフェイス要素のツールチップと、ビデオを再生できないときに表示されるエラーメッセージが含まれます。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOL と呼ばれる特別な Viewer SDK 識別子で表されます。 すべての SYMBOL には、デフォルトのビューアに付属する英語ロケール（`"en"`）のテキスト値が関連付けられています。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアは起動時、現在のロケールを調べて、そのロケールでサポートされている各 SYMBOL にユーザー定義の値があるかどうかを確認します。 デフォルト値が存在する場合は、ユーザー定義の値が使用され、存在しない場合は、標準のデフォルトテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケール、各ロケールの SYMBOL テキスト値、デフォルトのロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

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
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全画面表示ボタンが通常の状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> EmbedShare.TOOLTIP </span> を <span class="codeph"> します </p> </td> 
   <td colname="col2"> <p>「埋め込み共有」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.HEADER </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスの右上の「閉じる」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズ コンボボックス。 </p> </td> 
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
   <td colname="col1"> <p> EmbedShare.ACTION </span> を <span class="codeph"> します </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP アクション </span> </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> EmbedShare.CUSTOM_SIZE </span> を <span class="codeph"> します </p> </td> 
   <td colname="col2"> <p>埋め込みサイズ コンボボックスの最後の「カスタムサイズ」エントリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>リンク共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.HEADER </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスの右上の「閉じる」ボタン。 </p> </td> 
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
   <td colname="col2"> <p>「すべてを選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> LinkShare.TOOLTIP アクション </span> を <span class="codeph"> します </p> </td> 
   <td colname="col2"> <p>「すべてを選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「Facebook共有」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> TwitterShare.TOOLTIP </span> を <span class="codeph"> きます </p> </td> 
   <td colname="col2"> <p>「Twitter共有」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Video360Player.ERROR </span> </p> </td> 
   <td colname="col2"> <p>ビデオを再生できないときに表示されるエラーメッセージ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
