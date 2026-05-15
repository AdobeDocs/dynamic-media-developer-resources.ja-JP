---
title: ユーザーインターフェイス要素のローカライズ
description: インタラクティブ画像ビューアに表示される特定のコンテンツは、ローカライズの対象となります。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれています。
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
autotag-review: '2026-05-13T22:17:15.458Z'
TQID: 'https://experienceleague.adobe.com/XYvxUsA4fiBhf5gT35bxHZTo9Tn6QvT5ld89zNnHiOo'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライズ{#localization-of-user-interface-elements}

インタラクティブ画像ビューアに表示される特定のコンテンツは、ローカライズの対象となります。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれています。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOLと呼ばれる特別なビューアSDK IDで表されます。 任意のSYMBOLには、標準ビューアで指定された英語ロケール （`"en"`）のデフォルトの関連テキスト値が含まれており、必要に応じてユーザー定義の値が設定されている場合があります。

ビューアが起動すると、現在のロケールをチェックして、そのようなロケールでサポートされている各SYMBOLにユーザー定義の値があるかどうかを確認します。 存在する場合は、ユーザー定義の値を使用します。それ以外の場合は、デフォルトのデフォルトのテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされているロケールのリスト、各ロケールのSYMBOL テキスト値、およびデフォルトのロケールが含まれます。

そのようなローカライゼーションオブジェクトの例を以下に示します。

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

上記の例では、ローカライゼーションオブジェクトは2つのロケール（`"en"`と`"fr"`）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Web ページのコードは、ローカライゼーションオブジェクトを、設定オブジェクトの`localizedTexts` フィールドの値としてビューアコンストラクターに渡す必要があります。 別のオプションとして、`setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>ツールのヒント </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>最上位ビューア要素のARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザーのARIA使用ヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
