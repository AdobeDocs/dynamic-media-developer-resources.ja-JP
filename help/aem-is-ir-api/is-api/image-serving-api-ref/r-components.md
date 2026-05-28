---
title: 画像サービングコンポーネント
description: Dynamic Media画像サービングは、次のコンポーネントで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
TQID: 'https://experienceleague.adobe.com/T6NzrpcCTHA4MgFfCDtOxUPxTrcUAmX1zMG9jia4Zb8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 1%

---

# 画像サービングコンポーネント{#image-serving-components}

Dynamic Media画像サービングは、次のコンポーネントで構成されます。

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
   <td colname="col2"> <p>スタンドアロンの実行可能ファイル。他のコンポーネントの開始、停止、正常性の確保を担当します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>ほとんどのJava ベースのコンポーネントの環境を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/アラートサービス </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 サーバーの監視と電子メールアラートを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 クライアント接続、ログ、他のコンポーネントとの通信を管理します。 <span class="filepath"> /is/image</span>でのHTTP アクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching Service </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 [!DNL Platform Server]のデータ キャッシュを管理します。 /is/cacheでのHTTP アクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>画像処理と画像ファイルのI/O処理をすべて実行します。 Linux®では、32 ビットと64 ビットの両方の実行ファイルを利用できます（32 ビットはWindowsのみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE テキストレンダーコンポーネント </p> </td> 
   <td colname="col2"> <p><span class="codeph"> textPs=</span>操作を実行すると、テキストレンダリングサービスの1つ以上のインスタンスがアクティブになる可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG レンダーコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロン Java™ アプリケーション（Tomcatではホストされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering （別名： レンダーサーバー） </p> </td> 
   <td colname="col2"> <p>ライセンス認証には別のライセンスが必要です。 <span class="filepath"> /ir/render</span>でのHTTP アクセス。 すべての画像レンダリング機能は、[!DNL Platform Server]およびImage Serverに統合されており、個別の実行可能コンポーネントはありません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

追加の設定設定は、デフォルトカタログ（[!DNL default.ini]）または特定の画像カタログ（[画像カタログ &#x200B;](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照）によって提供されます。
