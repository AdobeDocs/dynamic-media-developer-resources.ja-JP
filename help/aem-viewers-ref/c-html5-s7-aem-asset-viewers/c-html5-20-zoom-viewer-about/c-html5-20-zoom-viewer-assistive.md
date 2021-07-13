---
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援技術のサポート
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム，アクセシビリティ
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性を持つ説明テキストが設定されます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

メインビューには役割`application`があります。 メインビューの簡単な説明は、 `aria-roledescription`に、対応するメインビューコンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に提供されます。 キーボードユーザーのナビゲーションヒントは、`aria-describedby`を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性にはそのラベルの値が設定されます。

スウォッチを表示するコンポーネントの役割`listbox`は、`aria-label`属性がそのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を表す`option`属性と`aria-setsize`属性が割り当てられています。 `aria-posinset`スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。
