---
description: 含む  [!DNL Platform Server]  設定。
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

[!DNL Platform Server] 設定が含まれます。

このファイルは JAVA プロパティファイルです。 適切な規則に従うように注意する必要があります。そうしないと、[!DNL Platform Server] が起動しない場合があります。 Windows ファイルのパスには、2 つのバックスラッシュ「\\」またはバックスラッシュ「/」を使用します。バックスラッシュ「\」は使用しません。 バックスラッシュは、このタイプのファイルでエスケープ文字として使用します。

このファイルに対する変更は、ファイルの保存後に有効になります。

[!DNL PlatformServer.conf] では、以下に示す設定のみを変更できます。 特定の設定がない場合は、ファイルの任意の場所に追加できます。 各設定のインスタンスは 1 つだけ存在できます。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>[!DNL Platform Server] の一般設定 </p> </td> 
  <td class="stentry"> <p> cache.rootPaths=を <span class="codeph"> します。/cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> staticContent.rootPaths=を <span class="codeph"> 定します。/static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>キャッシュクラスター設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>エラーのリダイレクト設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG設定 </p> </td> 
  <td class="stentry"> <p> svgProvider.rootPaths=を <span class="codeph"> します。/images </span> </p> <p> <span class="codeph">.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> svgProvider.fontRoot=を <span class="codeph"> します。/images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセットの応答 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
