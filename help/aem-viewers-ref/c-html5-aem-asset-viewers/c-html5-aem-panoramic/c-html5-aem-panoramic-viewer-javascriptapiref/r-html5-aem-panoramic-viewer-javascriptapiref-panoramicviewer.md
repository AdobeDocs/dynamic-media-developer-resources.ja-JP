---
title: PanoramicViewer
description: Constructorは、HTML5 Panoramic Viewer インスタンスを作成します。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 162
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
