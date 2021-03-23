---
description: フライアウトビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このようなコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどがあります。
seo-description: フライアウトビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このようなコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどがあります。
seo-title: ユーザーインターフェイス要素のローカライゼーション
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
uuid: efba09ad-200b-4540-8876-c9e462ec233a
feature: Dynamic Mediaクラシック，ビューア，SDK/API，フライアウト
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

フライアウトビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このようなコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどがあります。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 すべてのシンボルに、標準搭載のビューアに付属の英語ロケール(`"en"`)に対応するデフォルトのテキスト値があります。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアの開始は、現在のロケールをチェックし、ロケールでサポートされている各シンボルにユーザ定義の値があるかどうかを確認します。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトロケールが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

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

上記の例では、ローカライゼーションオブジェクトは2つのロケール（`"en"`と`"fr"`）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードは、設定オブジェクトの`localizedTexts`フィールドの値として、ローカライゼーションオブジェクトをビューアのコンストラクターに渡す必要があります。 別の方法として、`setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

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
   <td colname="col1"> <p> <span class="codeph"> コンテナ.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>最上位レベルのビューア要素のARIAラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示コンポーネントのARIAロールの説明です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー向けの使用上のヒントです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>デスクトップシステムに関する情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>タッチデバイスに関する情報メッセージです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>左スクロールボタンに関するツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>右スクロールボタンに関するツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>上スクロールボタンに関するツールチップ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>下スクロールボタンに関するツールチップ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

