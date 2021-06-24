---
description: 'Scene7画像サービングは、次のコンポーネントで構成されています '
solution: Experience Manager
title: 画像サービングコンポーネント
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---

# 画像サービングコンポーネント{#image-serving-components}

Scene7画像サービングは、次のコンポーネントで構成されています。

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>サーバースーパーバイザ </p> </td> 
   <td colname="col2"> <p>他のコンポーネントの起動、停止、および正常性の確保を担当するスタンドアロンの実行可能ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>ほとんどのJavaベースのコンポーネントの環境を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警告サービス </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 サーバーの監視とEメールの警告を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Platform Server </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 クライアント接続、ログ、他のコンポーネントとの通信を管理します。 <span class="filepath"> /is/image</span>でのHTTPアクセス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>キャッシュサービス </p> </td> 
   <td colname="col2"> <p>J2EEアプリケーション。 Platform Serverのデータキャッシュを管理します。 /is/cacheでのHTTPアクセス </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>すべての画像処理および画像ファイルのI/O操作を実行します。 32ビットと64ビットの実行可能ファイルは、Linuxで使用できます（Windowsの場合は32ビットのみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Render Component </p> </td> 
   <td colname="col2"> <p><span class="codeph"> textPs=</span>操作が実行されると、テキストレンダリングサービスの1つ以上のインスタンスがアクティブになる場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVGレンダリングコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロンJavaアプリケーション（Tomcatではホストされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media画像レンダリング( Render Server) </p> </td> 
   <td colname="col2"> <p>をアクティブ化するには、別のライセンスが必要です。 <span class="filepath"> /ir/render</span>でのHTTPアクセス。 すべての画像レンダリング機能は、個別の実行可能コンポーネントを使用せずに、Platform ServerとImage Serverに統合されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

追加の設定は、デフォルトのカタログ([!DNL default.ini])または特定の画像カタログ（詳しくは、[画像カタログ](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照）で提供されます。
