---
description: ビデオビューアで表示されるコンテンツには、ズームボタンやフルスクリーンボタンなど、ローカライゼーションの対象となるものもあります。
solution: Experience Manager
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

ビデオビューアで表示されるコンテンツには、ズームボタンやフルスクリーンボタンなど、ローカライゼーションの対象となるものもあります。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 すべてのシンボルに、標準搭載のビューアに付属の英語ロケール(`"en"`)に対応するデフォルトのテキスト値があります。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアの開始は、現在のロケールをチェックし、ロケールでサポートされている各シンボルにユーザ定義の値があるかどうかを確認します。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトロケールが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

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

上記の例では、ローカライゼーションオブジェクトは2つのロケール（`"en"`と`"fr"`）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードは、このようなローカライゼーションオブジェクトを設定オブジェクトの`localizedTexts`フィールドの値としてビューアのコンストラクタに渡す必要があります。 別の方法として、`setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>ツールチップの対象 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コンテナ.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>最上位レベルのビューア要素のARIAラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示コンポーネントのARIAロールの説明です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー向けの使用上のヒントです。 </p> </td> 
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
   <td colname="col2"> <p>通常の状態でのフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態でのフルスクリーンボタン。 </p> </td> 
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
 </tbody> 
</table>

