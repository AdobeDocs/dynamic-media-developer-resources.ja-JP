---
description: eCatalogビューアに表示されるコンテンツには、ズームボタン、ページ変更ボタン、サムネールボタン、全画面表示ボタン、閉じるボタン、スクロールバーボタンなど、ローカリゼーションの対象となるものもあります。
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: c44bfb38-a523-4399-8dbd-936830bb7cac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

eCatalogビューアに表示されるコンテンツには、ズームボタン、ページ変更ボタン、サムネールボタン、全画面表示ボタン、閉じるボタン、スクロールバーボタンなど、ローカリゼーションの対象となるものもあります。

ビューア内のテキスト内容は、ローカライズ可能ですべて、SYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 シンボルには、標準提供のビューアに付属する英語ロケール(`"en"`)に関連するデフォルトのテキスト値があり、必要な数のロケールに対してユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

ユーザー定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケールのリスト、各ロケールのSYMBOLテキスト値、およびデフォルトのロケールが含まれます。

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

Webページコードでは、設定オブジェクトの`localizedTexts`フィールドの値として、このようなローカリゼーションオブジェクトをビューアコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

次のシンボルがサポートされています（ここで「 containerId 」はビューアのコンテナのID）。

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
   <td colname="col2"> <p>ARIAラベル（トップレベルのビューア要素用） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT  </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>通常状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>全画面表示状態のフルスクリーンボタン。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_rightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>次の大きいページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_leftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>1つ前の大きいページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_lastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>最後のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>最後のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_firstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>最初のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>最初のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarRightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>次のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>前のページボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>サムネールモードのサムネールボタン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>通常モードのサムネールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>情報パネルの閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>電子メール共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>電子メールダイアログのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>電子メールダイアログボックスの右上の閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS  </span> </p> </td> 
   <td colname="col2"> <p>Eメールアドレスの形式が正しくない場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO  </span> </p> </td> 
   <td colname="col2"> <p>「宛先」入力フィールドのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD  </span> </p> </td> 
   <td colname="col2"> <p>別の電子メールアドレスを追加ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD  </span> </p> </td> 
   <td colname="col2"> <p>別の電子メールアドレスを追加ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM  </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドから。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE  </span> </p> </td> 
   <td colname="col2"> <p>メッセージ入力フィールド。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE  </span> </p> </td> 
   <td colname="col2"> <p>「電子メールアドレスを削除」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信後のダイアログの下部に表示される閉じるボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>フォームの送信後にダイアログの下部に表示される閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>フォーム送信ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS  </span> </p> </td> 
   <td colname="col2"> <p>Eメールが正常に送信された場合に表示される確認メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE  </span> </p> </td> 
   <td colname="col2"> <p>電子メールが正常に送信されなかった場合に表示されるエラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>埋め込み共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>埋め込みダイアログボックスの右上にある閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードテキストの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックスのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>埋め込みサイズコンボボックスの最後の「カスタムサイズ」エントリのテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>リンク共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>リンクダイアログボックスの右上にある閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>共有リンクの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>「すべて選択」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> 「すべて選択」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Facebook共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Twitter共有ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>印刷ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>印刷ダイアログのヘッダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>印刷ダイアログボックスの右上の閉じるボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE  </span> </p> </td> 
   <td colname="col2"> <p>「印刷ページを選択」セクションのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT  </span> </p> </td> 
   <td colname="col2"> <p>「現在のページ」ラジオボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM  </span> </p> </td> 
   <td colname="col2"> <p>「次から範囲を広げる」ラジオボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO  </span> </p> </td> 
   <td colname="col2"> <p>「宛先」数値選択のキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL  </span> </p> </td> 
   <td colname="col2"> <p>「すべてのページ」ラジオボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PRINT.PAGE_HANDLING  </span> </p> </td> 
   <td colname="col2"> <p>「ページ処理」セクションのラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE  </span> </p> </td> 
   <td colname="col2"> <p>「1シートあたり1ページ」ラジオボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO  </span> </p> </td> 
   <td colname="col2"> <p>「1シートあたり2ページ」ラジオボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>「キャンセル」ボタンのキャプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p> 「キャンセル」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>「印刷に送信」ボタンのキャプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> 「印刷に送信」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>お気に入りメニューボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>お気に入りを編集モードの「お気に入りを追加」ボタン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>通常モードで「お気に入りを追加」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>お気に入りの編集モードの「お気に入りを削除」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>通常モードで「お気に入りを削除」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>[お気に入り]ビューがアクティブな場合は、[すべてのお気に入りを表示]ボタンが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>[お気に入り]ビューが非アクティブな場合は、[お気に入りをすべて表示]ボタンをクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>1つのお気に入りアイコン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY]  </span> </p> </td> 
   <td colname="col2"> <p>読み込み時にビューアによって生成されるページラベル。 </p> <p>このシンボルの名前はテンプレートで、 <span class="codeph"> XX </span>は横方向の0を基準とする見開きインデックスで、オプションの<span class="codeph"> YY </span>は<span class="codeph"> XX </span>のターゲットとなる見開き内の0を基準とするページインデックスです。 </p> <p>最初に読み込まれたアセットにのみ適用されます。アセットが<span class="codeph"> setAsset() </span> API呼び出しを使用して変更された場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM  </span> </p> </td> 
   <td colname="col2"> <p> 見開きの左右のページにラベルを定義する場合に、ページラベルの区切り文字として使用される文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの左スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの右スクロールボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.PLACEHOLDER  </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが検索テキストの入力を開始する前に、検索入力ボックス内に表示されるローカライズされたプロンプト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_PROMPT  </span> </p> </td> 
   <td colname="col2"> <p>検索パネルを初めて開いたときに表示される、ユーザーに検索の実行を勧めるローカライズされたメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_NO_RESULTS  </span> </p> </td> 
   <td colname="col2"> <p>検索で結果が返されなかった場合に表示されるローカライズされたメッセージ。 </p> <p>このシンボルは、次のランタイム置換トークンをサポートします。<span class="codeph"> $SEARCH_TEXT$ </span>. コンポーネントは、ユーザーが入力した検索テキストに置き換えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_RESULTS  </span> </p> </td> 
   <td colname="col2"> <p>検索が正常に完了し、少なくとも1つの結果が返された場合に表示されるローカライズされたメッセージ。 </p> <p>このシンボルは、次のランタイム置換トークンをサポートします。 </p> <p> 
     <ul id="ul_30B76EAB921848069BE843A5F91F697A"> 
      <li id="li_16AF3EFCC4BF4180B66DE5EA82CC77F4"> <span class="codeph"> $SEARCH_TEXT$ — ユ </span> ーザーが入力した検索テキスト。 </li> 
      <li id="li_A0FBF12344B04BF0B702A2B7473330A8"> <span class="codeph"> $HIT_COUNT$ — 検 </span> 索で見つかったヒットの合計数。 </li> 
      <li id="li_9EB7B41A989B455ABEC72E052284F117"> <span class="codeph"> $PAGE_COUNT$  </span>  — 検索ヒットが1つ以上含まれるカタログページの数。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.THUMBNAIL_LABEL  </span> </p> </td> 
   <td colname="col2"> <p>検索パネルの結果サムネールのローカライズされたラベル。 </p> <p>このシンボルは、次のランタイム置換トークンをサポートします。 </p> <p> 
     <ul id="ul_7620C59FA56544CD9CE9E49B1871BCC1"> 
      <li id="li_FAF092734B4B4B55A309413690DA3FCC"> <span class="codeph"> $PAGE$  </span>  — ページ番号。 </li> 
      <li id="li_3414176505BB4A768FB42341A315E96F"> <span class="codeph"> $PAGE_HIT_COUNT$  </span>  — ページ内の検索結果の数。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>検索パネル全体の<span class="codeph"> aria-label </span> ARIA属性の値を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
