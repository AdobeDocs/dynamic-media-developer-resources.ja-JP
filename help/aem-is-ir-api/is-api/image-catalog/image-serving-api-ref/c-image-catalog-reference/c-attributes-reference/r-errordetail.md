---
description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。

次の値を指定できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの簡単な一般的な説明を返します。 公開されているライブサーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>短いメッセージ。 将来の使用のために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細メッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルパスなどの機密情報が含まれる場合があります。 ステージング、品質保証、およびアプリケーション開発サーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 適用可能な場合、Javaスタックトレースを追加します。 エラー画像にはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>にレベル2の情報が返されます。 この情報は、Dynamic Mediaテクニカルサポートに問題を報告する際に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値は、0、1、2、3のいずれかである必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

指定されていない場合や空の場合は`default::ErrorDetail`から継承されます。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
