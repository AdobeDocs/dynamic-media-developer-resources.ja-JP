---
description: レイヤー表示のプロパティ。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 10%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

レイヤー表示のプロパティ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| url | `xsd:string` | テンプレートを表す画像サーバーのURL。 `urlModifier`と`urlPostAp- plyModifier`のフィールドを組み合わせます。 |
| urlModifier | `xsd:string` | 要求または`urlPostApplyModifier` コマンドの前に適用する画像サービングプロトコルコマンド。 |
| urlPostApplyModifier | `xsd:string` | `urlModifier`および要求コマンドの後に適用するイメージ サービング プロトコル コマンド。 |
