---
title: PanoramicViewer
description: Constructorは、HTML5 Panoramic Viewer インスタンスを作成します。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%
---
# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructorは、HTML5 Panoramic Viewer インスタンスを作成します。

## パラメータ {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} オプションのJSON設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドの呼び出しを避けることができます。 次のプロパティが含まれています。

* containerId - ビューアが挿入されるDOM コンテナ （通常はDIV）の{String} ID。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありませんが、init （）が実行されるときにはコンテナが存在する必要があります。 必須
* params - {Object} ビューア設定パラメーターを持つJSON オブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子のいずれかであり、そのプロパティの値は対応する設定値です。 必須
* handlers - {Object} ビューア イベント コールバックを持つJSON オブジェクト。プロパティ名はサポートされているビューア イベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 ビューアイベントについて詳しくは、イベントコールバックの節を参照してください。 オプション。


## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
