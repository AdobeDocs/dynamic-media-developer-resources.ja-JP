---
title: ユーザーインターフェイス要素のローカライゼーション
description: カルーセルビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、スライドナビゲーションボタンが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

カルーセルビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、スライドナビゲーションボタンが含まれます。

ビューア内のテキスト内のローカライズ可能な内容は、SYMBOL と呼ばれる、特別な Viewer SDK 識別子で表されます。 SYMBOL には、英語のロケール ( `"en"`) が標準のビューアに付属しており、必要に応じてロケールのユーザ定義値も設定されている場合があります。

ビューアが起動すると、現在のロケールがチェックされ、そのロケールでサポートされる各シンボルに対してユーザ定義の値が存在するかどうかが確認されます。 ある場合は、ユーザー定義の値を使用します。それ以外の場合は、標準のデフォルトテキストにフォールバックされます。

ユーザ定義のローカリゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケール、各ロケールの SYMBOL テキスト値、およびデフォルトのロケールのリストが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態が選択されました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>再生/一時停止ボタンの状態が未選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> 前と次のスライドボタンのツールチップおよび ARIA ラベル。 </p> <p>次の 2 つの置換トークンを受け入れます。 <span class="codeph"> $CURRENT_FRAME$ </span> 現在のスライドインデックスと <span class="codeph"> $TOTAL_FRAMES$ </span> （スライドの合計数） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> トップレベルのビューア要素の ARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> メインビューコンポーネントの ARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA キーボードユーザー向けの使用ヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
