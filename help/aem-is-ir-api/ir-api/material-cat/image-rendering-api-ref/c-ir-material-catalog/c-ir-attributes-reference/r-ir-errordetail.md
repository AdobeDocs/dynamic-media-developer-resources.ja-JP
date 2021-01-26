---
description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
seo-description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 4%

---


# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。

## タイトル {#section-c10d75d72ee24d16a67cc8d927f1deba}

次の値を指定できます。

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの一般的な短い説明を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来的に使用するために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を表示します。 ファイルパスなど、機密性の高い情報を含めることができます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 該当する場合にJavaスタックトレースを追加します。 エラーイメージにはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>にレベル2の情報が返されます。 </p></td> 
 </tr> 
</table>

* 一般にアクセスできるライブサーバーにはレベル0をお勧めします。
* ステージング、品質保証およびアプリケーション開発サーバーには、レベル2が推奨されます。
* レベル3の情報は、Dynamic Mediaのテクニカルサポートに対するレポートの問題が発生した場合に役立ちます。

## プロパティ {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列挙値。0、1、2または3である必要があります。

## 初期設定 {#section-5e78d550050840cc9a1de811c581b94f}

指定しなかった場合や空の場合は`default::ErrorDetail`から継承。

## 関連項目 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
