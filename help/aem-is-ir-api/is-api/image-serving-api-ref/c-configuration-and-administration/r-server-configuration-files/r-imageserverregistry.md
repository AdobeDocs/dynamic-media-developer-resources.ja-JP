---
description: Image Serverの設定が含まれます。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Image Serverの設定が含まれます。

このXMLファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、Image Serverの起動に失敗する場合があります。

変更を有効にするには、このファイルを編集した後でImage Serverを再起動します。 変更では、以下に示す要素の値のみがサポートされます。 Dynamic Mediaテクニカルサポートの指示に従った場合にのみ、このファイルのその他のコンテンツを編集します。

>[!NOTE]
>
>要素の順序を含め、`<imageserverregistry>`の構造は変更しないでください。 このファイルを編集する際は注意が必要です。そうしないと、Image Serverの起動に失敗する場合があります。

次に、変更可能な要素を示します。 他の要素が存在し、この要素は変更できません。 以下の要素の順序は、ファイル内に存在する必要がある順序を反映しません。

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

複数の`<RootPath>`要素が存在する場合があります（ソースデータファイルフォルダーごとに1つ）。 Image Serverは、指定された順序でルートパスを検索し、特定のソースファイルを見つけます。
