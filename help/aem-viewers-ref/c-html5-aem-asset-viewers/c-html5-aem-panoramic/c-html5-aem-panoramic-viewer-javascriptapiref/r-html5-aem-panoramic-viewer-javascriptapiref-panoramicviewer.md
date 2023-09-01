---
title: PanoramicViewer
description: コンストラクター。HTML5 パノラマビューアインスタンスを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
コンストラクター。HTML5 パノラマビューアインスタンスを作成します。

## パラメータ {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} オプションの JSON 設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドを呼び出さないようにします。 次のプロパティが含まれます。

* containerId - {String} ビューアの挿入先の DOM コンテナ（通常は DIV）の ID。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありませんが、init() を実行する際にはコンテナが存在する必要があります。 必須
* params - {Object} ビューアの設定パラメーターを持つ JSON オブジェクト。プロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 必須
* ハンドラー — {Object} ビューアのイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 ビューアイベントについて詳しくは、イベントコールバックの節を参照してください。 オプション。


## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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
