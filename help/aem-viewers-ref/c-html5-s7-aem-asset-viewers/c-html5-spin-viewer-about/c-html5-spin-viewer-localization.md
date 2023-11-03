---
title: ユーザーインターフェイス要素のローカライゼーション
description: スピンビューアに表示されるコンテンツには、ズームボタンやフルスクリーンボタンなど、ローカライゼーションの対象となるものもあります。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: f4c0f16b-dbb9-4505-a3f2-d504ae21c3f0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

スピンビューアに表示されるコンテンツには、ズームボタンやフルスクリーンボタンなど、ローカライゼーションの対象となるものもあります。

ビューア内のテキスト内のローカライズ可能なコンテンツは、SYMBOL と呼ばれる、特別な Viewer SDK 識別子で表されます。 SYMBOL には、英語のロケール ( `"en"`) には、標準のビューアが付属しています。 また、必要な数のロケールに対して、ユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、ロケールでサポートされる各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値を使用します。それ以外の場合は、標準のデフォルトテキストにフォールバックされます。

ユーザ定義のローカリゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケールのリスト、各ロケールの SYMBOL テキスト値、およびデフォルトロケールが含まれます。

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

上記の例では、ローカリゼーションオブジェクトで 2 つのロケール ( `"en"` および `"fr"`) を参照し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページコードでは、ローカリゼーションオブジェクトをの値としてビューアのコンストラクターに渡す必要があります。 `localizedTexts` 設定オブジェクトのフィールド。 別のオプションとして、 `setLocalizedTexts(localizationInfo)` メソッド。

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
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA キーボードユーザー向けの使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「閉じる」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームインボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームアウトボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームのリセットボタン。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>左にスピンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>右へスピンボタン。 </p> </td> 
  </tr> 
 </tbody> 
</table>
