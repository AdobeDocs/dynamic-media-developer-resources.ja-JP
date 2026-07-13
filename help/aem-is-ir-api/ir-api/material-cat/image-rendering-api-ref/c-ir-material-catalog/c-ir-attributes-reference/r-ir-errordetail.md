---
title: ErrorDetail
description: エラーメッセージの詳細。 HTTPを介して返されるエラーメッセージの詳細レベルをerror.message値として指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
TQID: 'https://experienceleague.adobe.com/34sgN8GefR-rkAcikbnE3p3Yh6-1xJXEMfEg6Q74yLM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTPを介して返されるエラーメッセージの詳細レベルをerror.message値として指定します。

## タイトル {#section-c10d75d72ee24d16a67cc8d927f1deba}

次の値を使用できます。

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの短い一般的な説明を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>ブリーフメッセージ： 将来の使用のために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細メッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルのパスなどの機密情報が含まれる場合があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報 該当する場合は、Java™ スタックトレースを追加します。 エラー画像にはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>でレベル 2の情報を返します。 </p></td> 
 </tr> 
</table>

* レベル 0は、一般にアクセスできるライブサーバーに推奨されます。
* レベル 2は、ステージング、品質保証、アプリケーション開発サーバーに推奨されます。
* レベル 3の情報は、Dynamic Media テクニカルサポートに問題を報告する際に役立つ場合があります。

## プロパティ {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列挙値。0、1、2、または3にする必要があります。

## 初期設定 {#section-5e78d550050840cc9a1de811c581b94f}

指定されていない場合や空の場合は、`default::ErrorDetail`から継承されます。

## 関連項目 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)

