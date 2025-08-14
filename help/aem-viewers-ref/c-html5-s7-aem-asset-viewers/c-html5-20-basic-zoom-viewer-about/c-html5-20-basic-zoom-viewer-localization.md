---
title: ユーザーインターフェイス要素のローカリゼーション
description: 基本ズームビューアに表示される特定のコンテンツは、ローカライゼーション（ズームボタン、フルスクリーンボタンなど）の影響を受けます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8c399b64-e278-41bc-a9eb-692812979fea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

基本ズームビューアに表示される特定のコンテンツは、ローカライゼーション（ズームボタン、フルスクリーンボタンなど）の影響を受けます。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOL と呼ばれる特別なビューアSDK識別子で表されます。 どの SYMBOL にも、すぐに使用できるビューアに用意されている英語ロケール（`"en"`）のデフォルトのテキスト値が関連付けられています。また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアは起動時、現在のロケールを調べて、ロケールでサポートされる各記号にユーザー定義の値があるかどうかを確認します。 デフォルト値が存在する場合は、ユーザー定義の値が使用され、存在しない場合は、標準のデフォルトテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケール、各ロケールの SYMBOL テキスト値、デフォルトのロケールのリストが含まれます。

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

上記の例では、localization オブジェクトは 2 つのロケール（`"en"` と `"fr"`）を定義し、各ロケールで 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページのコードは、このようなローカリゼーションオブジェクトを、設定オブジェクトのフィールドの値としてビューアのコンストラクター `localizedTexts` 渡す必要があります。 別のオプションとして、メソッドを呼び出してローカリゼーションオブジェクト `setLocalizedTexts(localizationInfo)` 渡すこともできます。

次の記号がサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>記号 </p> </th> 
   <th colname="col2" class="entry"> <p>...のツールチップ </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>最上位のビューア要素の ARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ZoomView.ROLE_DESCRIPTION <span class="codeph"> を </span> きます。 </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA 役割の説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザー向けの ARIA 使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「閉じる」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>「ズームイン」ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームアウトボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>ズームリセットボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全画面表示ボタンが通常の状態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
 </tbody> 
</table>
