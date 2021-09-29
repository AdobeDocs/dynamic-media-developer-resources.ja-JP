---
title: 支援技術のサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

トップレベルのビューア要素には、デフォルトでビューアの名前に設定された役割 `region` と `aria-label` 属性があります。 ラベルは `Container.LABEL` ローカリゼーション記号で制御できます。

メインビューには役割 `application` があります。 メインビューの簡単な説明は、 `aria-roledescription` に記載され、対応するメインビューコンポーネントの `ROLE_DESCRIPTION` ローカライゼーション記号で定義された値と共に示されます。 キーボードユーザーのナビゲーションヒントは `aria-describedby` を使用して提供され、使用ヒントのテキストは `USAGE_HINT` ローカライゼーション記号から取得されます。 アセットの UserData フィールドにラベルが定義されている場合、`aria-label` 属性にはそのラベルの値が設定されます。

ホットスポット、領域、および画像マップには、`button` 属性を持つ役割と説明テキストが設定され、ホットスポットまたは画像マップラベルの値が設定されます。 `aria-label`ユーザーがホットスポットや画像マップにフォーカスを置くと、キーボードユーザーのナビゲーションヒントが `aria-describedby` を使用して提供され、使用ヒントのテキストは `USAGE_HINT` ローカライゼーションシンボルから取得されます。
