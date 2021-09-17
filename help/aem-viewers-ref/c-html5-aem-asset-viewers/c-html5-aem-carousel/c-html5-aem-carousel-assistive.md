---
title: 支援技術のサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性を持つ説明テキストが設定されます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

カルーセルのスライド間を移動するためのボタンには、現在選択されているスライドに応じて実行時に更新されるラベルがあります。 これらのボタンラベルのテンプレートは、 `CAROUSELVIEWER_TOOLTIP_GOTO`ローカライゼーション記号で設定されます。

メインビューには役割`application`があります。 メインビューの簡単な説明は、 `aria-roledescription`に、対応するメインビューコンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に提供されます。 キーボードユーザーのナビゲーションヒントは、`aria-describedby`を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性にはそのラベルの値が設定されます。

ホットスポット、領域、および画像マップには、役割`button`と`aria-label`属性で設定された説明テキストが割り当てられ、ホットスポットまたは画像マップラベルの値が割り当てられます。 ユーザーがホットスポットや画像マップにフォーカスを置くと、キーボードユーザーのナビゲーションヒントが`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーションシンボルから取得されます。
