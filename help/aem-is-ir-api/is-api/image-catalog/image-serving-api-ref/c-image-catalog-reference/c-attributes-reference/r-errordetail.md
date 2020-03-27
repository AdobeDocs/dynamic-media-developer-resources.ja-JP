---
description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
seo-description: エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorDetail{#errordetail}

エラーメッセージの詳細。 HTTP経由で返されるエラーメッセージの詳細レベルをerror.message値として指定します。

次の値を使用できます。

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>タイトルのみ。 エラーの一般的な簡単な説明を返します。 公開してアクセスできるライブサーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡単なメッセージ。 将来の使用のために予約。 現在、0と同じ情報を返します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細なメッセージ。 エラーに関するユーザーレベルの詳細を提供します。 ファイルパスなど、機密性の高い情報が含まれる場合があります。 ステージング、品質保証およびアプリケーション開発サーバーに推奨されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全なデバッグ情報。 該当する場合は、Javaスタックトレースを追加します。 エラー画像にはスタックトレースが含まれず、代わりにレベル2の情報が <span class="codeph"> $error.messageに返されます</span>。 この情報は、Scene7テクニカルサポートに問題を報告する際に役立ちます。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-e167895723ca4ad4ba283d3d7b4324de}

列挙値。0、1、2または3である必要があります。

## 初期設定 {#section-8f27098e509945a18676aca0675c8f41}

指定しなかっ `default::ErrorDetail` た場合または空の場合に継承。

## 関連項目 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
