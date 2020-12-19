---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、初期設定でビューア名に設定されているロール`region`と`aria-label`の属性があります。 ラベルはローカライゼーション記号`Container.LABEL`で制御できます。

メイン表示は`application`の役割を持ちます。 メイン表示の簡単な説明は、`aria-roledescription`に記載され、対応するメイン表示コンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に記載されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性は、このラベルの値で設定されます。

スウォッチを表示するコンポーネントには、`listbox`の役割(`aria-label`属性が、そのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています)が割り当てられます。 個々のスウォッチには、セット内のスウォッチの位置を示す役割`option`と`aria-setsize`属性と`aria-posinset`属性があります。 スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。
