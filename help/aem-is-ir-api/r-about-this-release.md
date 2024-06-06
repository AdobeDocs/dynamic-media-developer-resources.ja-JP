---
description: このリリース（画像サービング 6.6.1 および画像レンダリング 6.6.1）は、画像サービング 6.5.3 および画像レンダリング 6.5.3 より優先されます。
solution: Experience Manager
title: このリリースについて
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# このリリースについて{#about-this-release}

このリリース（画像サービング 6.6.1 および画像レンダリング 6.6.1）は、画像サービング 6.5.3 および画像レンダリング 6.5.3 より優先されます。

## 既知の問題と動作の変更 {#section-9dbc05206187477f926a78e8108a34e1}

* アセット ID での疑問符文字の使用は、文字が URL エンコードされている場合でも、サポートされなくなりました。
* 動的バナー `/xfl/flash/` リクエストがサポートされなくなり、HTTP 404 エラーコードを返すようになりました。
* W2P `/is/agm/` リクエストがサポートされなくなりました。
* 一部のエラーメッセージは、ブラウザーにレンダリングされなくなりました。 そのため、デバッグするには、トレースログを確認する必要があります。

## 新機能 {#section-b1386e36cb4544ebb79766a06b16842d}

* スマートスウォッチ
* スマート切り抜き

## バグ修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* が発生する問題を修正しました `\qc` RTF オプションの後にスペースが続くことで、要求がレンダリングされませんでした。
