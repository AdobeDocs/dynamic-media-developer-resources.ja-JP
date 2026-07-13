---
description: データファイルのパス。 この画像に関連付けられている画像以外のデータファイルの相対パスと名前。
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
TQID: 'https://experienceleague.adobe.com/p1AZ2QZmQpKM9D-gvBCxavzsdWlLjb-MSO-kluc05oE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 3%

---

# AuxPath{#auxpath}

データファイルのパス。 この画像に関連付けられている画像以外のデータファイルの相対パスと名前。

サーバーは、この値をattribute::RootPathと組み合わせて、実際のファイルパスを構築します。 絶対ファイルパスでもかまいません。

キャビネット マテリアルのキャビネット スタイル ファイルまたはウィンドウ カバーマテリアルのウィンドウ カバースタイル ファイルを指定するために使用します。 他のすべてのマテリアルに対しては空のままにします。

## プロパティ {#section-4268350054b7421da0ce0327f0731a52}

テキスト文字列値。 指定する場合は、有効な相対または絶対ファイルパスである必要があります。 キャビネット材料および窓被覆材料に必要です。 他のすべてのマテリアルに対して空にする必要があります。

## 初期設定 {#section-287005c2d8e948fa958f69ba7b90b437}

なし

## 関連項目 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)、[&#x200B; カタログ：:Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)、[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)

