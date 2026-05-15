---
description: エラーメッセージの詳細。 HTTPを介して返されるエラーメッセージの詳細レベルをerror.message値として指定します。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTPを介して返されるエラーメッセージの詳細レベルをerror.message値として指定します。

次の値を使用できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの短い一般的な説明を返します。 一般にアクセスできるライブサーバー向けに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>ブリーフメッセージ： 将来の使用のために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細メッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルのパスなどの機密情報が含まれる場合があります。 ステージング、品質保証、アプリケーション開発サーバー向けに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報 該当する場合は、Java スタックトレースを追加します。 エラー画像にはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>でレベル 2の情報を返します。 この情報は、Dynamic Media テクニカルサポートに問題を報告する際に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値。0、1、2、または3にする必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

指定されていない場合や空の場合は、`default::ErrorDetail`から継承されます。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
