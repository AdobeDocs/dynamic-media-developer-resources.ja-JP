---
description: インタラクティブ画像ビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。
title: ユーザーインターフェイス要素のローカライゼーション
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

インタラクティブ画像ビューアに表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。

ビューア内のテキスト内容がローカライズ可能な場合は、それぞれSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 シンボルには、標準提供のビューアに付属する英語ロケール(`"en"`)のデフォルトの関連テキスト値があり、必要な数のロケールに対してユーザ定義の値を設定することもできます。

ビューアが起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義の値があるかどうかが確認されます。 ある場合は、ユーザー定義の値が使用されます。それ以外の場合は、標準のデフォルトテキストに戻ります。

ユーザー定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このようなオブジェクトには、サポートされているロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトのロケールが含まれます。

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

上の例では、ローカリゼーションオブジェクトは2つのロケール（ `"en"`と`"fr"` ）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードでは、設定オブジェクトの`localizedTexts`フィールドの値として、ローカリゼーションオブジェクトをビューアのコンストラクターに渡す必要があります。 別のオプションとして、 `setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡す方法があります。

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
   <td colname="col2"> <p>トップレベルビューア要素のARIAラベル </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIAキーボードユーザー用の使用ヒント </p> </td> 
  </tr> 
 </tbody> 
</table>
