---
description: Image Server の設定が含まれます。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Image Server の設定が含まれます。

この XML ファイルを変更する場合、有効な XML 構文を維持するよう注意する必要があります。そうしないと、Image Server の起動に失敗する可能性があります。

変更を有効にするには、このファイルを編集した後、Image Server を再起動します。 以下に示す要素の値のみが変更できます。 このファイルのその他の内容は、Dynamic Media テクニカルサポートから連絡があった場合にのみ編集してください。

>[!NOTE]
>
>要素の順序を含め、`<imageserverregistry>` の構造を変更しないでください。 このファイルを編集する場合は注意が必要です。編集しないと、Image Server の起動に失敗する可能性があります。

以下に、変更可能な要素を示します。 変更してはいけない他の要素が存在します。 以下の要素の順序は、ファイル内での要素の存在順序を反映していません。

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

複数の `<RootPath>` 要素が存在する場合があります（ソースデータファイルフォルダーごとに 1 つ）。 Image Server は、指定された順序でルートパスを検索して、特定のソースファイルを検索します。
