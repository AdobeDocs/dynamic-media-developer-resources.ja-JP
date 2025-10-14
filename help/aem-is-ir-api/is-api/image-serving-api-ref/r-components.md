---
title: 画像サービングコンポーネント
description: Dynamic Media 画像サービングは、次のコンポーネントで構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# 画像サービングコンポーネント{#image-serving-components}

Dynamic Media 画像サービングは、次のコンポーネントで構成されています。

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>サーバースーパーバイザー </p> </td> 
   <td colname="col2"> <p>他のコンポーネントの起動、停止、および正常性の確保を担当するスタンドアロンの実行可能ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>ほとんどの Java ベースのコンポーネントに環境を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警告サービス </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 サーバーの監視と電子メールアラートを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 クライアント接続、ログ、他のコンポーネントとの通信を管理します。 /is/image<span class="filepath"></span>HTTP アクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>キャッシュサービス </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 [!DNL Platform Server] のデータ キャッシュを管理します。 /is/cache での HTTP アクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>すべての画像処理および画像ファイルの I/O 操作を実行します。 Linux® では、32 ビットと 64 ビットの両方の実行可能ファイルを使用できます（32 ビットは Windows のみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>テキストレンダリングコンポーネントの作成 </p> </td> 
   <td colname="col2"> <p>textPs=<span class="codeph"> 操作が実行されると、テキストレンダリングサービスの 1 つ以上のインスタンスがアクティブ </span> なる場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG レンダリングコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロン Java™ アプリケーション（Tomcat はホストしていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media 画像レンダリング（別名： レンダリングサーバー） </p> </td> 
   <td colname="col2"> <p>ライセンス認証には別のライセンスが必要です。 /ir/render<span class="filepath"> で </span>HTTP アクセス。 すべての画像レンダリング機能は、[!DNL Platform Server] と Image Server に統合されており、別個の実行可能コンポーネントはありません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

追加の設定は、デフォルトカタログ（[!DNL default.ini]）または特定の画像カタログ（詳しくは [&#x200B; 画像カタログ &#x200B;](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) を参照）によって提供されます。
