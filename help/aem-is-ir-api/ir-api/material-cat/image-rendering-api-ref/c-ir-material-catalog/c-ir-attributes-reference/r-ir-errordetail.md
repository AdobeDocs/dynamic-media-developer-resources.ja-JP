---
description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。

## タイトル {#section-c10d75d72ee24d16a67cc8d927f1deba}

次の値を指定できます。

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの簡単な一般的な説明を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>短いメッセージ。 将来の使用のために予約されています。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細メッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルパスなどの機密情報が含まれる場合があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 適用可能な場合、Javaスタックトレースを追加します。 エラー画像にはスタックトレースが含まれず、代わりに<span class="codeph"> $error.message</span>にレベル2の情報が返されます。 </p></td> 
 </tr> 
</table>

* 公にアクセスできるライブサーバーには、レベル0をお勧めします。
* ステージング、品質保証、およびアプリケーション開発サーバーには、レベル2をお勧めします。
* レベル3の情報は、Dynamic Mediaテクニカルサポートに問題を報告する際に役立つ場合があります。

## プロパティ {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列挙値は、0、1、2、3のいずれかである必要があります。

## 初期設定 {#section-5e78d550050840cc9a1de811c581b94f}

指定されていない場合や空の場合は`default::ErrorDetail`から継承されます。

## 関連項目 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
