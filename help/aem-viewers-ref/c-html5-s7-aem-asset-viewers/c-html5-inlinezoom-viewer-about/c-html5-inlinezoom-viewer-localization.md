---
description: フライアウトビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

フライアウトビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。

ビューア内のテキスト内容がローカライズ可能な場合は、それぞれSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 シンボルには、標準提供のビューアに付属する英語ロケール(`"en"`)のデフォルトの関連テキスト値があり、必要な数のロケールに対してユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

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

Webページコードでは、設定オブジェクトの`localizedTexts`フィールドの値として、このようなローカリゼーションオブジェクトをビューアのコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

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
