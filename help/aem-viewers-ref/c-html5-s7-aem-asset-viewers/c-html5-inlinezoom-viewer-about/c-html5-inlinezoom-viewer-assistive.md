---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

トップレベルのビューア要素には役割があります `region` および `aria-label` 属性は、デフォルトでビューアの名前に設定されます。 ラベルは `Container.LABEL` ローカリゼーションシンボル。

メインビューには役割があります `application`. メインビューの簡単な説明は、 `aria-roledescription`の値を、 `ROLE_DESCRIPTION` 対応するメインビューコンポーネントのローカライゼーションシンボル。 キーボードユーザーのナビゲーションヒントは、 `aria-describedby`の場合、使用のヒントのテキストは `USAGE_HINT` ローカリゼーションシンボル。 アセットに UserData フィールドで定義されたラベルがある場合、 `aria-label` 属性は、そのようなラベルの値で設定されます。

スウォッチを表示するコンポーネントには、役割があります `listbox` と `aria-label` 属性を `LABEL` そのコンポーネントのローカライゼーションシンボル。 個々のスウォッチには役割があります `option` と `aria-setsize` および `aria-posinset` 属性は、セット内のスウォッチの位置を表します。 スウォッチが選択されている場合、 `aria-selected` 属性を `true`.
