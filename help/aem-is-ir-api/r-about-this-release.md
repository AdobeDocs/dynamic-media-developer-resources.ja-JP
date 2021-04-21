---
description: このリリース（画像サービング6.6.1および画像レンダリング6.6.1）は、画像サービング6.5.3および画像レンダリング6.5.3に置き換えられました。
solution: Experience Manager
title: このリリースについて
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# このリリースについて{#about-this-release}

このリリース（画像サービング6.6.1および画像レンダリング6.6.1）は、画像サービング6.5.3および画像レンダリング6.5.3に置き換えられました。

## 既知の問題と動作の変更{#section-9dbc05206187477f926a78e8108a34e1}

* アセットIDでの疑問符の使用は、文字がURLエンコードされている場合でもサポートされなくなりました。
* 動的バナー`/xfl/flash/`のリクエストはサポートされなくなり、http 404エラーコードを返すようになりました。
* W2P `/is/agm/`リクエストはサポートされなくなりました。
* 一部のエラーメッセージがブラウザーに表示されなくなりました。 したがって、デバッグするトレースログを確認する必要があります。

## 新機能 {#section-b1386e36cb4544ebb79766a06b16842d}

* スマートスウォッチ
* スマート切り抜き

## バグ修正{#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTFオプションの後にスペースが続くと、リクエストがレンダリングされない問題を修正しました。

