---
description: インタラクティブ画像ビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどが含まれます。
seo-description: インタラクティブ画像ビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどが含まれます。
seo-title: ユーザーインターフェイス要素のローカライゼーション
title: ユーザーインターフェイス要素のローカライゼーション
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# ユーザーインターフェイス要素のローカライゼーション{#localization-of-user-interface-elements}

インタラクティブ画像ビューアで表示されるコンテンツには、ローカライゼーションの対象となるものもあります。 これには、ユーザインターフェイス要素のツールチップや、読み込み時にフライアウトズーム表示によって表示される情報メッセージなどが含まれます。

ローカライズ可能なビューア内のテキストコンテンツは、すべてSYMBOLと呼ばれる特別なビューアSDK識別子で表されます。 すべてのシンボルには、標準搭載のビューアに付属の英語ロケール(`"en"`)に対するデフォルトの関連テキスト値があり、また、必要な数のロケールに対してユーザ定義値を設定できます。

ビューアの開始は、現在のロケールをチェックして、そのロケールでサポートされている各シンボルに対してユーザ定義値があるかどうかを確認します。 存在する場合は、ユーザー定義の値が使用されます。それ以外の場合は、そのまま使用できるデフォルトのテキストに戻ります。

ユーザ定義のローカライゼーションデータは、ローカライゼーションJSONオブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされるロケールのリスト、各ロケールのシンボルテキスト値、およびデフォルトロケールが含まれます。

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

上の例では、ローカライゼーションオブジェクトは2つのロケール（`"en"`と`"fr"`）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Webページコードは、設定オブジェクトの`localizedTexts`フィールドの値として、ローカライゼーションオブジェクトをビューアのコンストラクターに渡す必要があります。 別の方法として、`setLocalizedTexts(localizationInfo)`メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

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
 </tbody> 
</table>

