---
title: ErrorDetail
description: エラーメッセージの詳細。 HTTP 経由で返されるエラーメッセージの詳細レベルを error.message 値として指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 5%

---

# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP 経由で返されるエラーメッセージの詳細レベルを error.message 値として指定します。

## タイトル {#section-c10d75d72ee24d16a67cc8d927f1deba}

次の値を指定できます。

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの短い一般的な説明を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>概要メッセージ。 将来の使用のために予約されています。 現在、0 と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルのパスなどの機密情報が含まれる場合があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 該当する場合は、Java™スタックトレースを追加します。 エラー画像にスタックトレースが含まれず、代わりにでレベル 2 の情報が返される <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* 公にアクセスできるライブサーバーには、レベル 0 をお勧めします。
* ステージング、品質保証、およびアプリケーション開発サーバーには、レベル 2 をお勧めします。
* レベル 3 の情報は、Dynamic Mediaテクニカルサポートに問題を報告する際に役立つ場合があります。

## プロパティ {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列挙値は、0、1、2、3 のいずれかである必要があります。

## 初期設定 {#section-5e78d550050840cc9a1de811c581b94f}

継承元 `default::ErrorDetail` 指定されていない場合、または空の場合は。

## 関連項目 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
