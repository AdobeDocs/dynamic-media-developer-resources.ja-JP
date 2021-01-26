---
description: 'Scene 7画像サービングは、次のコンポーネントで構成されています '
seo-description: 'Scene 7画像サービングは、次のコンポーネントで構成されています '
seo-title: 画像サービングコンポーネント
solution: Experience Manager
title: 画像サービングコンポーネント
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 2%

---


# 画像サービングコンポーネント{#image-serving-components}

Scene 7画像サービングは、次のコンポーネントで構成されています。

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>サーバスーパーバイザ </p> </td> 
   <td colname="col2"> <p>他のコンポーネントの起動、停止、および正常性の確保を行うスタンドアロン実行可能ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>ほとんどのJavaベースのコンポーネントの環境を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警告サービス </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 サーバの監視と電子メールによるアラート機能を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>プラットフォームサーバー </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 クライアント接続、ログ、他のコンポーネントとの通信を管理します。 <span class="filepath"> /is/image</span>でHTTPアクセスします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>キャッシュサービス </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 Platform Serverのデータキャッシュを管理します。 /is/cacheでのHTTPアクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>イメージ処理とイメージファイルのI/O処理をすべて実行します。 32-bitと64-bitの両方の実行可能ファイルは、Linuxで使用できます（32-bit版はWindows版のみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Renderコンポーネント </p> </td> 
   <td colname="col2"> <p><span class="codeph"> textPs=</span>操作が実行されると、テキストレンダリングサービスの1つ以上のインスタンスがアクティブになる場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVGレンダリングコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロンJavaアプリケーション（Tomcatでホストされるものではない）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Mediaイメージレンダリング( Render Server) </p> </td> 
   <td colname="col2"> <p>ライセンス認証を行うには別のライセンスが必要です。 <span class="filepath"> /ir/render</span>でのHTTPアクセス。 すべてのイメージレンダリング機能は、個別の実行可能コンポーネントを使用せずに、Platform ServerとImage Serverに統合されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

追加の設定は、デフォルトのカタログ([!DNL default.ini])または特定の画像カタログ（詳しくは、[画像カタログ](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照）で提供されます。
