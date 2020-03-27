---
description: フライアウトビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。
seo-description: フライアウトビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。
seo-title: ユーザーインターフェイス要素のローカリゼーション
solution: Experience Manager
title: ユーザーインターフェイス要素のローカリゼーション
topic: Dynamic media
uuid: d824c0c3-3606-4903-96f7-de26a61a8f65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

フライアウトビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 任意のシンボルには、標準搭載のビューアに付属する英語のロケール( `"en"`)に対する初期設定の関連テキスト値が含まれ、また、必要な数のロケールに対してユーザ定義の値が設定される場合があります。

ビューアを起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義値が存在するかどうかが確認されます。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカリゼーションデータは、ローカリゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケール、各ロケールのシンボルテキスト値、およびデフォルトロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
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
   <td colname="col2"> <p>ARIAの最上位ビューア要素のラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIAのキーボードユーザー向けの使用方法のヒントです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>デスクトップシステムに関する情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>タッチデバイスに関する情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>左スクロールボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>右スクロールボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>上スクロールボタンのツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>下スクロールボタンに関するツールチップ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

