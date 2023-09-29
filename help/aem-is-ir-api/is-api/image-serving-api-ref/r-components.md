---
title: 画像サービングコンポーネント
description: Dynamic Media画像サービングは、次のコンポーネントで構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 画像サービングコンポーネント{#image-serving-components}

Dynamic Media画像サービングは、次のコンポーネントで構成されています。

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
   <td colname="col2"> <p>他のコンポーネントの起動、停止、および正常性の確保を担当するスタンドアロン実行可能ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>これにより、ほとんどの Java ベースのコンポーネントに対して環境が提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警告サービス </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 サーバーの監視と E メールの警告機能を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 クライアント接続、ログ、他のコンポーネントとの通信を管理します。 HTTP アクセス： <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>キャッシュサービス </p> </td> 
   <td colname="col2"> <p>J2EE アプリケーション。 を管理する [!DNL Platform Server]のデータキャッシュを使用します。 /is/cache での HTTP アクセス </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>すべての画像処理および画像ファイルの I/O 操作を実行します。 Linux®では、32 ビットと 64 ビットの実行可能ファイルの両方が使用可能です（Windows の場合は 32 ビットのみ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Render Component </p> </td> 
   <td colname="col2"> <p>テキストレンダリングサービスの 1 つ以上のインスタンスが、 <span class="codeph"> textPs=</span> 操作が実行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVGレンダリングコンポーネント </p> </td> 
   <td colname="col2"> <p>スタンドアロン Java™アプリケーション（Tomcat ではホストされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media画像レンダリング ( Render Server) </p> </td> 
   <td colname="col2"> <p>ライセンス認証を行うには、別のライセンスが必要です。 HTTP アクセス： <span class="filepath"> /ir/render</span>. すべての画像レンダリング機能は、 [!DNL Platform Server] と Image Server に別個の実行可能コンポーネントが存在しない。 </p> </td> 
  </tr> 
 </tbody> 
</table>

デフォルトのカタログ ( [!DNL default.ini]) または特定の画像カタログ ( [画像カタログ](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) を参照 )。
