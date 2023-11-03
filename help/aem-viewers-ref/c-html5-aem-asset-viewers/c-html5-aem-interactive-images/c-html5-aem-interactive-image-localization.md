---
title: ユーザーインターフェイス要素のローカライゼーション
description: インタラクティブ画像ビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

インタラクティブ画像ビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。

ビューア内のテキスト内のローカライズ可能な内容は、SYMBOL と呼ばれる、特別な Viewer SDK 識別子で表されます。 SYMBOL には、英語のロケール ( `"en"`) が標準のビューアに付属しており、必要に応じてロケールのユーザ定義値が設定されている場合もあります。

ビューアが起動すると、現在のロケールがチェックされ、そのロケールでサポートされる各シンボルに対してユーザ定義の値が存在するかどうかが確認されます。 ある場合は、ユーザー定義の値を使用します。それ以外の場合は、標準のデフォルトテキストにフォールバックされます。

ユーザ定義のローカリゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされるロケール、各ロケールの SYMBOL テキスト値、およびデフォルトのロケールのリストが含まれます。

このようなローカライゼーションオブジェクトの例を次に示します。

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA キーボードユーザー向けの使用ヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
