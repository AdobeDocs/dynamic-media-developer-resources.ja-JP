---
title: ErrorDetail
description: エラーメッセージの詳細。 HTTP によって error.message 値として返されるエラーメッセージの詳細レベルを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP によって error.message 値として返されるエラーメッセージの詳細レベルを指定します。

## タイトル {#section-c10d75d72ee24d16a67cc8d927f1deba}

次の値を使用できます。

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの簡単な一般的な説明を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来の使用のために予約済み。 現在は、0 と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルパスなどの機密情報が含まれる場合があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報 該当する場合、Java™ スタックトレースを追加します。 エラー画像にスタックトレースが含まれることはなく、代わりに$error.message<span class="codeph"> のレベル 2 情報 </span> 返します。 </p></td> 
 </tr> 
</table>

* レベル 0 は、公開としてアクセスできるライブサーバーに推奨されます。
* ステージング サーバー、品質保証サーバー、アプリケーション開発サーバーにはレベル 2 をお勧めします。
* レベル 3 の情報は、Dynamic Media テクニカルサポートに問題を報告する際に役立つ場合があります。

## プロパティ {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列挙値。0、1、2、3 のいずれかである必要があります。

## 初期設定 {#section-5e78d550050840cc9a1de811c581b94f}

指定されていない場合または空の場合に `default::ErrorDetail` から継承されます。

## 関連項目 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
