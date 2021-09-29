---
title: ユーザーインターフェイス要素のローカライゼーション
description: インタラクティブ画像ビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザーインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

インタラクティブ画像ビューアに表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 このコンテンツには、ユーザーインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージなどが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべて SYMBOL と呼ばれる特別なビューア SDK 識別子で表されます。 シンボルには、標準提供のビューアに付属する英語のロケール (`"en"`) のデフォルトのテキスト値が関連付けられ、必要な数のロケールに対してユーザ定義の値が設定されている場合があります。

ビューアが起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

ユーザ定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされているロケール、各ロケールの SYMBOL テキスト値、およびデフォルトのロケールのリストが含まれます。

このようなローカリゼーションオブジェクトの例を次に示します。

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

上記の例では、ローカリゼーションオブジェクトは 2 つのロケール（ `"en"` と `"fr"` ）を定義し、各ロケールの 2 つのユーザーインターフェイス要素のローカライゼーションを提供します。

Web ページコードでは、ローカリゼーションオブジェクトを設定オブジェクトの `localizedTexts` フィールドの値としてビューアのコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

次のシンボルがサポートされています。

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
   <td colname="col2"> <p>ARIA トップレベルビューア要素のラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントの ARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA のキーボードユーザー用の使用のヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
