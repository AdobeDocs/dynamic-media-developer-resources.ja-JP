---
description: Image Serverの設定設定が含まれます。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
TQID: 'https://experienceleague.adobe.com/UdMACutToNmpsXnhU0jAaItCZJ8r0RTxirjaqXSpa0c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Image Serverの設定設定が含まれます。

このXML ファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、Image Serverが起動しない可能性があります。

変更を有効にするには、このファイルを編集した後にImage Serverを再起動します。 以下に示す要素値のみが変更でサポートされます。 このファイルのその他のコンテンツは、Dynamic Media テクニカルサポートからアドバイスを受けた場合にのみ編集します。

>[!NOTE]
>
>要素の順序を含め、`<imageserverregistry>`の構造を変更しないでください。 このファイルを編集する場合は注意してください。そうしないと、Image Serverが起動しない可能性があります。

次に、変更できる要素を示します。 その他の要素が存在します。これは変更できません。 以下のエレメントの順序は、ファイルに存在する必要がある順序を反映していません。

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

複数の`<RootPath>`要素が存在する可能性があります（ソースデータファイルフォルダーごとに1つ）。 Image Serverは、特定のソースファイルを検索するために、指定された順序でルートパスを検索します。
