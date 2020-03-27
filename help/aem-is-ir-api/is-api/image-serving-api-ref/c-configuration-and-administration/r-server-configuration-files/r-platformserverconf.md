---
description: プラットフォームサーバーの設定が含まれます。
seo-description: プラットフォームサーバーの設定が含まれます。
seo-title: PlatformServer.conf
solution: Experience Manager
title: PlatformServer.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: d798762b-c9ff-4e1b-b2ac-c5e40476b375
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PlatformServer.conf{#platformserver-conf}

プラットフォームサーバーの設定が含まれます。

このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意しなければならない。そうしないと、プラットフォームサーバーの起動に失敗する場合があります。 Windowsファイルパスでは、バックスラッシュ「\」の代わりに、二重のバックスラッシュ「\\」または単一のスラッシュ「/」を使用します。 バックスラッシュは、このタイプのファイルではエスケープ文字として使用されます。

このファイルに対する変更は、ファイルの保存後に有効になります。

で変更できるのは、次に示す設定のみで [!DNL PlatformServer.conf]す。 特定の設定がない場合は、ファイル内の任意の場所に追加できます。 各設定のインスタンスは1つだけ存在できます。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般的なプラットフォームサーバーの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>キャッシュクラスタの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;空&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>リダイレクト設定のエラー </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;空&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./イメージ </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./イメージ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセットの回答 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>

