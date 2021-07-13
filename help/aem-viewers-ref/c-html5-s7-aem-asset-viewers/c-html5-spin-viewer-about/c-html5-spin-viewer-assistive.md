---
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援技術のサポート
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット，アクセシビリティ
role: Developer,User
exl-id: f0cde820-237c-4594-8a16-d272af4c976b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性を持つ説明テキストが設定されます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

メインビューには役割`application`があります。 メインビューの簡単な説明は、 `aria-roledescription`に、対応するメインビューコンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に提供されます。 キーボードユーザーのナビゲーションヒントは、`aria-describedby`を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性にはそのラベルの値が設定されます。
