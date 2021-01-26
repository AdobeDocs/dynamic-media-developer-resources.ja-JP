---
description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 5%

---


# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。

次の値を指定できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの一般的な短い説明を返します。 一般にアクセスできるライブサーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来的に使用するために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を表示します。 ファイルパスなど、機密性の高い情報を含めることができます。 ステージング、品質保証およびアプリケーション開発サーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 該当する場合にJavaスタックトレースを追加します。 エラーイメージにはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>にレベル2の情報が返されます。 この情報は、Dynamic Mediaのテクニカルサポートにレポートが問題を起こした場合に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値。0、1、2または3である必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

指定しなかった場合や空の場合は`default::ErrorDetail`から継承。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
