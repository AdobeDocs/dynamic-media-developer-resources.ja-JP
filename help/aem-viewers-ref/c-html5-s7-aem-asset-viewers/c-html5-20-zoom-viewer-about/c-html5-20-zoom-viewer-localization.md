---
title: ユーザーインターフェイス要素のローカライズ
description: ビデオビューアに表示される特定のコンテンツは、ズームボタンや全画面ボタンなど、ローカライゼーションの対象となります。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
TQID: 'https://experienceleague.adobe.com/5hQZ-XHITbIg6-bvxeMNMi71rau9xVOk3tsUIkQWyrk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 326
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライズ{#localization-of-user-interface-elements}

ビデオビューアに表示される特定のコンテンツは、ズームボタンや全画面ボタンなど、ローカライゼーションの対象となります。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOLと呼ばれる特別なビューアSDK IDで表されます。 任意のSYMBOLには、標準ビューアで指定された英語ロケール （`"en"`）のデフォルトの関連テキスト値があります。 また、必要な数のロケールに対してユーザー定義の値を設定することもできます。

ビューアが起動すると、現在のロケールをチェックして、ロケールでサポートされている各SYMBOLにユーザー定義の値があるかどうかを確認します。 存在する場合は、ユーザー定義の値を使用します。それ以外の場合は、デフォルトのデフォルトのテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされているロケールのリスト、各ロケールのSYMBOL テキスト値、およびデフォルトのロケールが含まれます。

そのようなローカライゼーションオブジェクトの例を以下に示します。

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

Web ページコードは、このようなローカライゼーションオブジェクトを設定オブジェクトの`localizedTexts` フィールドの値としてビューアコンストラクターに渡す必要があります。 別のオプションとして、`setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>ツールヒント： </p> </th> 
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
   <td colname="col2"> <p>ズームリセットボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンを通常の状態で使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーン状態のフルスクリーンボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>左ボタンをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>右スクロール ボタン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スクロールアップボタン： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>下にスクロール ボタン。 </p> </td> 
  </tr> 
 </tbody> 
</table>

