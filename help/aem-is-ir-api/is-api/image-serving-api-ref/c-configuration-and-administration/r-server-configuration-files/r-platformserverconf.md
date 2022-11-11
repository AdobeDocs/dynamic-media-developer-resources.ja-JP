---
description: 次を含む [!DNL Platform Server] 設定。
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# PlatformServer.conf{#platformserver-conf}

次を含む [!DNL Platform Server] 設定。

このファイルは、JAVA プロパティファイルです。 適切な規則に従うように注意しなければならない。それ以外の場合は、 [!DNL Platform Server] を開始できない可能性があります。 Windows のファイルパスでは、バックスラッシュ「\」の代わりに、バックスラッシュ「\」またはスラッシュ「/」を 1 つ使用します。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されます。

このファイルに対する変更は、ファイルの保存後に有効になります。

以下に示す設定のみを [!DNL PlatformServer.conf]. 特定の設定がない場合は、ファイルの任意の場所に追加できます。 各設定のインスタンスは 1 つだけ存在します。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般 [!DNL Platform Server] 設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>キャッシュクラスターの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>リダイレクト設定エラー </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./イメージ </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./イメージ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット応答 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
