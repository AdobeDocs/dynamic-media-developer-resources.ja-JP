---
title: setParam
description: スマート切り抜きビデオビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 193719b8-f158-4ffc-9916-b7b1bf36b2de
TQID: 'https://experienceleague.adobe.com/KXOrfuS5NgmGdUkx7AcgbtJxjcIuDYOU7nnUom42b-w'
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
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%
---
# setParam{#setparam}

スマート切り抜きビデオビューアのJavaScript API リファレンス。

` setParam( *`name, value`*)`

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメーターは`init()`の前に呼び出されます。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡された場合、このメソッドはオプションです。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名</span> </span> </p> </td> 
   <td colname="col2"> <p> パラメーターの<span class="codeph"> {string} </span>名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> パラメーターの値。 値をパーセント エンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
