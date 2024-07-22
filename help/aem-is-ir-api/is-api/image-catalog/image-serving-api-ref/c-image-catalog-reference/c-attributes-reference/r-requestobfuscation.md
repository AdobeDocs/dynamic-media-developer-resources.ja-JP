---
description: リクエスト暗号化モード。 有効なリクエストに適用する必要がある不明化のタイプを指定します。
solution: Experience Manager
title: RequestObfuscation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c330c8de-9539-442f-a52a-786f882873cf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---

# RequestObfuscation{#requestobfuscation}

リクエスト暗号化モード。 有効なリクエストに適用する必要がある不明化のタイプを指定します。

## プロパティ {#section-0819432615324e259f24717e16835427}

列挙値。 0 に設定するとリクエストの不明化が無効になり、1 に設定すると base64 エンコーディングが選択されます。 現時点では、他の不明化メソッドはサポートされていません。

## 初期設定 {#section-e7f49493d9a940acb4f7938df7cac44d}

定義されていない場合または空の場合は `default::RequestObfuscation` から継承します。
