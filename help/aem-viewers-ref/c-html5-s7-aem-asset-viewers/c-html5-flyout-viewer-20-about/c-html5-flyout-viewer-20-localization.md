---
description: フライアウトビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: 57941e90-1462-43e6-80db-6b111e004f9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

フライアウトビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。

ビューア内のテキスト内容は、ローカライズ可能ですべて、SYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 シンボルには、標準提供のビューアに付属する英語のロケール(`"en"`)に関連するデフォルトのテキスト値が関連付けられています。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

ユーザー定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトのロケールが含まれます。

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

上の例では、ローカリゼーションオブジェクトは2つのロケール（ `"en"`と`"fr"` ）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードでは、設定オブジェクトの`localizedTexts`フィールドの値として、ローカリゼーションオブジェクトをビューアのコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>トップレベルビューア要素のARIAラベル </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>デスクトップシステムの情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>タッチデバイス用の情報メッセージ。 </p> </td> 
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
