---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

メインビューにはロール `application` があります。 メインビューの簡単な説明が `aria-roledescription` に提供され、対応するメインビューコンポーネントの `ROLE_DESCRIPTION` のローカリゼーションシンボルによって定義された値が提供されます。 キーボードユーザー向けのナビゲーションヒントは `aria-describedby` を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT` のローカリゼーション記号から取得されます。 アセットの UserData フィールドにラベルが定義されている場合、`aria-label` 属性はそのラベルの値で設定されます。

ホットスポット、地域および画像マップには、役割 `button` と、ホットスポットまたは画像マップのラベルの値を `aria-label` つ属性を持つ説明テキストが設定されています。 ユーザーがホットスポットまたは画像マップにフォーカスを置くと、`aria-describedby` を使用してキーボードユーザーに対するナビゲーションヒントが提供され、使用ヒントのテキストは `USAGE_HINT` のローカライズ記号から得られます。
