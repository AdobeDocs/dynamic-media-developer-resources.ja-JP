---
description: 混在メディアビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ズームボタン、スピンボタン、ビデオコントロール、閉じるボタン、フルスクリーンボタン、スウォッチのスクロールボタンが含まれます。
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 119d8dde-145b-4762-a1ab-882a29e0f6a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

混在メディアビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ズームボタン、スピンボタン、ビデオコントロール、閉じるボタン、フルスクリーンボタン、スウォッチのスクロールボタンが含まれます。

ビューア内のテキスト内容は、ローカライズ可能ですべて、SYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 シンボルには、標準提供のビューアに付属する英語のロケール(`"en"`)に関連するデフォルトのテキスト値が関連付けられています。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

ユーザー定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトのロケールが含まれます。

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

上の例では、ローカリゼーションオブジェクトは2つのロケール（ `"en"`と`"fr"` ）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードでは、設定オブジェクトの`localizedTexts`フィールドの値として、ローカリゼーションオブジェクトをビューアコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>ツールチップ </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>トップレベルビューア要素のARIAラベル </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー用の使用ヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー用の使用ヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー用の使用ヒント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>ズームインボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>ズームアウトボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>ズームリセットボタン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">インライン</span>ズームモードのデスクトップシステム。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">インライン</span>ズームモードのタッチデバイス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>通常状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>全画面表示状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションボタンが選択された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションボタンが選択されていない状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>左スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>右スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>上スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>下スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>左スピンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>右へスピンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態を選択 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンが選択解除された状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーのビデオ時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームの選択状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームの選択を解除。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p>ARIA <span class="codeph"> aria-valuetext </span>属性を介して公開されるボリュームスライダノブラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>再生可能なビデオがない場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
