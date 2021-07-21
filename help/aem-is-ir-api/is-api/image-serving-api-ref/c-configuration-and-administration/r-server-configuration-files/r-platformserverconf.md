---
description: Platform Server設定が含まれます。
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# PlatformServer.conf{#platformserver-conf}

Platform Server設定が含まれます。

このファイルは、JAVAプロパティファイルです。 適切な規則に従うように注意しなければならない。そうしないと、Platform Serverの起動に失敗する場合があります。 Windowsのファイルパスでは、バックスラッシュ(\)の代わりに、バックスラッシュ(\\)を二重に、またはスラッシュ(/)を1つ使用します。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されます。

このファイルに対する変更は、ファイルを保存した後に有効になります。

[!DNL PlatformServer.conf]では、以下に示す設定のみを変更できます。 特定の設定がない場合は、ファイルの任意の場所に追加できます。 各設定のインスタンスは1つだけ存在します。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般的なPlatform Serverの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000  </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824  </span> </p> <p> <span class="codeph"> isConnection.port=27345  </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true  </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000  </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>キャッシュクラスターの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50  </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000  </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>リダイレクト設定エラー </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000  </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVGの設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./イメージ </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024  </span> </p> <p> <span class="codeph"> svgProvider.port=8080  </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./イメージ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセットの応答 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false  </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10  </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20  </span> </p> </td> 
 </tr> 
</table>
