---
description: CDN無効化リクエストで提供されたURLの1つに応答する詳細メッセージ。
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---

# OperationFault{#operationfault}

CDN無効化リクエストで提供されたURLの1つに応答する詳細メッセージ。

**次の日からサポート**

4.5.0（パッチ2011年2月）

## パラメータ {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名前** | ** 種類** | ** 説明** |
|---|---|---|
| `*`コード`*` | `xsd:int` | CDNから提供されるエラーコード |
| `*`理由`*` | `xsd:string` | CDNから提供されたエラーメッセージ |
