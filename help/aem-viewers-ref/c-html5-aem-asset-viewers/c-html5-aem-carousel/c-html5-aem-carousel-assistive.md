---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援テクノロジーのサポート
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー，アクセシビリティ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、初期設定でビューア名に設定されているロール`region`と`aria-label`の属性があります。 ラベルはローカライゼーション記号`Container.LABEL`で制御できます。

ボタンには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、`aria-disabled`属性がそれに応じて設定されます。

カルーセルスライド間を移動するためのボタンには、ラベルが含まれており、ラベルは現在選択されているスライドに応じて実行時に更新されます。 これらのボタンのラベルのテンプレートは、`CAROUSELVIEWER_TOOLTIP_GOTO`ローカライゼーション記号で設定されます。

メイン表示は`application`の役割を持ちます。 メイン表示の簡単な説明は、`aria-roledescription`に記載され、対応するメイン表示コンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に記載されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性は、このラベルの値で設定されます。

ホットスポット、領域および画像マップには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定され、ホットスポットまたは画像マップのラベルの値が設定されます。 ユーザーがホットスポットや画像マップにフォーカスすると、キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーションシンボルから取得されます。
