---
description: 'Scene 7画像サービングは、次のコンポーネントで構成されています '
solution: Experience Manager
title: 画像サービングコンポーネント
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
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
   <td colname="col2"> <p>J2EEアプリケーション。 プラットフォームサーバーのデータキャッシュを管理します。 /is/cacheでのHTTPアクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>すべてのイメージ処理とイメージファイルのI/O処理を実行します。 32ビットと64ビットの実行可能ファイルはどちらも、Linuxで使用できます（32ビットのWindowsのみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Renderコンポーネント </p> </td> 
   <td colname="col2"> <p><span class="codeph"> textPs=</span>操作が実行されると、テキストレンダリングサービスの1つ以上のインスタンスがアクティブになる場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVGレンダリングコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロンのJavaアプリケーション（Tomcatではホストされません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media画像レンダリング( Render Server) </p> </td> 
   <td colname="col2"> <p>ライセンス認証を行うには別のライセンスが必要です。 <span class="filepath"> /ir/render</span>でHTTPアクセスを行います。 すべての画像レンダリング機能は、実行可能コンポーネントが別々になく、プラットフォームサーバとImage Serverに統合されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

追加の設定は、初期設定のカタログ([!DNL default.ini])または特定の画像カタログ（詳しくは、[画像カタログ](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照）で提供されます。
