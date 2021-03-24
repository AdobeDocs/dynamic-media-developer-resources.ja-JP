---
description: リクエストの不明化モード 有効なリクエストに適用する必要がある不明化の種類を指定します。
solution: Experience Manager
title: RequestObfuscation
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 2%

---


# RequestObfuscation{#requestobfuscation}

リクエストの不明化モード 有効なリクエストに適用する必要がある不明化の種類を指定します。

## プロパティ {#section-0819432615324e259f24717e16835427}

列挙。 要求の不明化を無効にするには0に設定し、base64エンコーディングを選択するには1に設定します。 現時点では、他の不明化方法はサポートされていません。

## 初期設定 {#section-e7f49493d9a940acb4f7938df7cac44d}

定義されていない場合や空の場合は`default::RequestObfuscation`から継承されます。
