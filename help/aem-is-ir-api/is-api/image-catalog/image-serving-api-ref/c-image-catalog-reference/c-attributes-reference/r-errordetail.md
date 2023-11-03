---
description: エラーメッセージの詳細。 HTTP を介して返されるエラーメッセージの詳細レベルを error.message 値として指定します。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP を介して返されるエラーメッセージの詳細レベルを error.message 値として指定します。

次の値を指定できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの短い一般的な説明を返します。 公開されているライブサーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来の使用のために予約されています。 現在、0 と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルのパスなどの機密情報が含まれる場合があります。 ステージング、品質保証、およびアプリケーション開発サーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 該当する場合、Java スタックトレースを追加します。 エラー画像にスタックトレースが含まれず、代わりにでレベル 2 の情報が返される <span class="codeph"> $error.message</span>. この情報は、Dynamic Mediaテクニカルサポートに問題を報告する際に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値は、0、1、2、3 のいずれかである必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

継承元 `default::ErrorDetail` 指定されていない場合、または空の場合は。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
