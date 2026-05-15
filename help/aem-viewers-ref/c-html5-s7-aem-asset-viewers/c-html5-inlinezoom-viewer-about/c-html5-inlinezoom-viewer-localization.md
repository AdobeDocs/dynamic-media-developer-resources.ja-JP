---
title: ユーザーインターフェイス要素のローカライズ
description: フライアウトビューアに表示される特定のコンテンツは、ローカライズの対象となります。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
TQID: 'https://experienceleague.adobe.com/XuHwpAVZOG7ZbQsZay1Lov3UXFGkTNzTgsaf5xvnSKo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 341
ht-degree: 0%

---

# ユーザーインターフェイス要素のローカライズ{#localization-of-user-interface-elements}

フライアウトビューアに表示される特定のコンテンツは、ローカライズの対象となります。 このコンテンツには、ユーザーインターフェイス要素のツールヒントと、読み込み時にフライアウトズームビューで表示される情報メッセージが含まれています。

ローカライズ可能なビューア内のすべてのテキストコンテンツは、SYMBOLと呼ばれる特別なビューアSDK IDで表されます。 任意のSYMBOLには、標準ビューアで指定された英語ロケール （`"en"`）のデフォルトの関連テキスト値が含まれており、必要に応じてユーザー定義の値が設定されている場合もあります。

ビューアが起動すると、現在のロケールをチェックして、そのようなロケールでサポートされている各SYMBOLにユーザー定義の値があるかどうかを確認します。 存在する場合は、ユーザー定義の値を使用します。それ以外の場合は、デフォルトのデフォルトのテキストにフォールバックします。

ユーザー定義のローカライゼーションデータは、ローカライゼーション JSON オブジェクトとしてビューアに渡すことができます。 このオブジェクトには、サポートされているロケールのリスト、各ロケールのSYMBOL テキスト値、およびデフォルトのロケールが含まれます。

そのようなローカライゼーションオブジェクトの例を以下に示します。

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

上記の例では、ローカライゼーションオブジェクトは2つのロケール（`"en"`と`"fr"`）を定義し、各ロケールの2つのユーザーインターフェイス要素にローカライゼーションを提供します。

Web ページのコードは、このようなローカライゼーションオブジェクトを、設定オブジェクトの`localizedTexts` フィールドの値としてビューアコンストラクターに渡す必要があります。 別のオプションとして、`setLocalizedTexts(localizationInfo)` メソッドを呼び出してローカライゼーションオブジェクトを渡すこともできます。

次のシンボルがサポートされています。

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>シンボル </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>最上位ビューア要素のARIA ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>メインビューコンポーネントのARIA ロールの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>キーボードユーザーのARIA使用ヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>デスクトップシステムの情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>タッチデバイス向けの情報メッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>左スクロール ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>右スクロール ボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スクロールアップボタンのツールヒント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>スクロールダウンボタンのツールヒント。 </p> </td> 
  </tr> 
 </tbody> 
</table>
