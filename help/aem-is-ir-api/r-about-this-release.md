---
description: このリリース（Image Serving 6.6.1およびImage Rendering 6.6.1）は、Image Serving 6.5.3およびImage Rendering 6.5.3に取って代わります。
solution: Experience Manager
title: このリリースについて
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# このリリースについて{#about-this-release}

このリリース（Image Serving 6.6.1およびImage Rendering 6.6.1）は、Image Serving 6.5.3およびImage Rendering 6.5.3に取って代わります。

## 既知の問題と動作の変更 {#section-9dbc05206187477f926a78e8108a34e1}

* アセット IDでの疑問符の使用は、URL エンコードされた文字であっても、サポートされなくなりました。
* 動的なバナー`/xfl/flash/`要求はサポートされなくなったため、HTTP 404 エラーコードが返されるようになりました。
* W2P `/is/agm/`要求はサポートされなくなりました。
* 一部のエラーメッセージがブラウザーにレンダリングされなくなりました。 そのため、デバッグするには、トレースログを確認する必要があります。

## 新機能 {#section-b1386e36cb4544ebb79766a06b16842d}

* スマートスウォッチ
* スマートクロップ

## バグ修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTF オプションの後にスペースが続くと、リクエストがレンダリングされない問題を修正しました。
