---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 6312f2f7-e1fa-4536-bae4-d8bc7735d5af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、初期設定でビューア名に設定されているロール`region`と`aria-label`の属性があります。 ラベルはローカライゼーション記号`Container.LABEL`で制御できます。

ボタンには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、`aria-disabled`属性がそれに応じて設定されます。

メイン表示は`application`の役割を持ちます。 メイン表示の簡単な説明は、`aria-roledescription`に記載され、対応するメイン表示コンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に記載されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性は、このラベルの値で設定されます。
