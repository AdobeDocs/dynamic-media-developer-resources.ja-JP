---
description: インタラクティブ画像ビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。
seo-description: インタラクティブ画像ビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。
seo-title: ユーザーインターフェイス要素のローカリゼーション
title: ユーザーインターフェイス要素のローカリゼーション
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ユーザーインターフェイス要素のローカリゼーション{#localization-of-user-interface-elements}

インタラクティブ画像ビューアで表示されるコンテンツには、ローカリゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールヒントや、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 任意のシンボルには、標準搭載のビューアに付属する英語のロケール( `"en"`)に対する初期設定の関連テキスト値が含まれ、また、必要な数のロケールに対してユーザ定義の値が設定される場合があります。

ビューアを起動すると、現在のロケールがチェックされ、そのロケールでサポートされている各シンボルに対してユーザ定義値が存在するかどうかが確認されます。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカリゼーションデータは、ローカリゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケール、各ロケールのシンボルテキスト値、およびデフォルトロケールのリストが含まれます。

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

上の例では、ローカリゼーションオブジェクトは2つのロケール(および `"en"` )を定義し、 `"fr"`各ロケールの2つのユーザーインターフェイス要素のローカリゼーションを提供します。

Webページコードは、設定オブジェクトのフィールドの値として、ローカリゼーションオブジェクトをビューアのコ `localizedTexts` ンストラクターに渡す必要があります。 別の方法として、メソッドを呼び出してローカリゼーションオブジェクトを渡す方法が `setLocalizedTexts(localizationInfo)` あります。

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIAの最上位ビューア要素のラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIAロールの説明です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIAのキーボードユーザー向けの使用方法のヒントです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

