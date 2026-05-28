---
description: 4種類のレイヤーがサポートされています。
solution: Experience Manager
title: レイヤータイプ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
TQID: 'https://experienceleague.adobe.com/F2ZE-uepvnDVG2OImJIzXm44Wm3KLYfLZrBnk11tE6I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 0%

---

# レイヤータイプ{#layer-types}

4種類のレイヤーがサポートされています。

## 画像レイヤー {#section-3e53df1437694272aca03f927fc0db07}

画像レイヤーには、レイヤーとして使用する画像を指定する`src=` コマンドが必要です。 レイヤーマスクとして使用する`mask=`で別の画像を指定するか、画像に既にアルファチャンネルが含まれている場合があります。 画像レイヤーのサイズは常に画像から派生しますが、画像は`size=` コマンドを使用して適切に拡大・縮小されることがよくあります。 クリップパスは`clipPath=`に適用できます。

## テキストレイヤー {#section-dc2aec6416a340bcb20c1f884323c8d0}

リッチテキスト形式（RTF）のテキストフラグメントの形式でテキストコンテンツを提供する`text=`または`textPs=` コマンドが必要です。 テキストレイヤーは、コンテンツに合わせてセルフサイズにすることも、明示的なサイズを指定することもできます。 例えば、テキストを特定の幅に折り返す場合や、テキストを特定の領域内で拘束する必要がある場合などです。 `textPs=`は、`textFlowPath=`で定義された任意のシェイプと、`textPath=`で定義された任意のパスへのテキストの流れをサポートしています。 `textPs=`は、テキストボックスまたは任意の角度（`textAngle=`）で指定された図形へのテキストのレンダリングもサポートしています。

## べた塗りのレイヤー {#section-56dfb672756643dda08dc93294809eb0}

単色レイヤーは、テンプレートのレイヤー0によく使用されるため、合成画像のサイズは固定され、画像コンテンツとは独立しています。 べた塗りのレイヤーには、`color=`属性と`size=`または`mask=`が必要です。また、外観を変更するためのほとんどのコマンドと属性をサポートしています。 べた塗りのレイヤーは、`clipPath=`を持つ任意のシェイプを指定できます。

## エフェクトレイヤー {#section-dd3b628bc6734077af4c0ddcebcee05f}

ドロップシャドウや光彩エフェクトなどのPhotoshopスタイルのレイヤーエフェクトは、画像、テキスト、および単色レイヤーに添付できる特殊なサブレイヤーを使用してISによって実装されます。 これらのエフェクトレイヤーは、親レイヤーのマスクと位置を親レイヤーから継承し、機能が制限されています。
