---
description: エラーメッセージの詳細。 HTTP によって error.message 値として返されるエラーメッセージの詳細レベルを指定します。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP によって error.message 値として返されるエラーメッセージの詳細レベルを指定します。

次の値を使用できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの簡単な一般的な説明を返します。 公開でアクセス可能なライブサーバーの場合に推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来の使用のために予約済み。 現在は、0 と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルパスなどの機密情報が含まれる場合があります。 ステージング サーバー、品質保証サーバー、およびアプリケーション開発サーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報 該当する場合、Java スタックトレースを追加します。 エラー画像にスタックトレースが含まれることはなく、代わりに$error.message<span class="codeph"> のレベル 2 情報 </span> 返します。 この情報は、Dynamic Media テクニカルサポートに問題を報告する際に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値。0、1、2、3 のいずれかである必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

指定されていない場合または空の場合に `default::ErrorDetail` から継承されます。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
