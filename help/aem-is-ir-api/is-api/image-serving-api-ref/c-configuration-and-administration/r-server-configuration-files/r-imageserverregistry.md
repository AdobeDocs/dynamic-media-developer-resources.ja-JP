---
description: Image Serverの設定が含まれます。
seo-description: Image Serverの設定が含まれます。
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Image Serverの設定が含まれます。

このXMLファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、Image Serverで開始が失敗する場合があります。

変更を有効にするには、このファイルを編集した後でImage Serverを再起動します。 変更できるのは、次に示す要素の値のみです。 このファイルの他の内容は、Scene7テクニカルサポートの指示に従う場合にのみ編集してください。

>[!NOTE]
>
>`<imageserverregistry>`の構造（要素の順序も含む）は変更しないでください。 このファイルを編集する場合は注意が必要です。注意が必要でないと、Image Serverの開始に失敗する場合があります。

次に、変更可能な要素を示します。 変更できない他の要素が存在する。 以下の要素の順序は、ファイル内に存在する必要がある順序を反映しません。

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## 説明 {#section-7217f011f69f41e7af4f3983d7776d6f}

複数の`<RootPath>`要素が存在する場合があります（ソースデータファイルのフォルダーごとに1つずつ）。 Image Serverは、指定された順序でルートパスを検索し、特定のソースファイルを見つけます。
