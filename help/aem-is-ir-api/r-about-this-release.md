---
description: このリリース（画像サービング6.6.1および画像レンダリング6.6.1）は、画像サービング6.5.3および画像レンダリング6.5.3に置き換わりました。
solution: Experience Manager
title: このリリースについて
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# このリリースについて{#about-this-release}

このリリース（画像サービング6.6.1および画像レンダリング6.6.1）は、画像サービング6.5.3および画像レンダリング6.5.3に置き換わりました。

## 既知の問題と動作の変更点 {#section-9dbc05206187477f926a78e8108a34e1}

* アセットIDでの疑問符文字の使用は、その文字がURLエンコードされている場合でもサポートされなくなりました。
* 動的バナー`/xfl/flash/`のリクエストはサポートされなくなり、HTTP 404エラーコードが返されるようになりました。
* W2P `/is/agm/`リクエストはサポートされなくなりました。
* 一部のエラーメッセージは、ブラウザーに表示されなくなりました。 そのため、デバッグのためにトレースログを確認する必要があります。

## 新機能 {#section-b1386e36cb4544ebb79766a06b16842d}

* スマートスウォッチ
* スマート切り抜き

## バグ修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTFオプションの後にスペースが続くと、リクエストがレンダリングされない問題を修正しました。
