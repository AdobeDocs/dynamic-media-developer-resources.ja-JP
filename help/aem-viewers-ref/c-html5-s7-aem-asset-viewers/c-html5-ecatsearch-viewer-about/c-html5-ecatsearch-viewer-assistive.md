---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援テクノロジーのサポート
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog検索，アクセシビリティ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、初期設定でビューア名に設定されているロール`region`と`aria-label`の属性があります。 ラベルはローカライゼーション記号`Container.LABEL`で制御できます。

ボタンには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、`aria-disabled`属性がそれに応じて設定されます。

メイン表示は`application`の役割を持ちます。 メイン表示の簡単な説明は、`aria-roledescription`に記載され、対応するメイン表示コンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に記載されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性は、このラベルの値で設定されます。

ホットスポット、領域および画像マップには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定され、ホットスポットまたは画像マップのラベルの値が設定されます。 ユーザーがホットスポットや画像マップにフォーカスすると、キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーションシンボルから取得されます。

サムネールには、`ThumbnailGridView.LABEL`ローカライゼーション記号で制御される`aria-label`属性を持つ`dialog`ロールがあります。 個々のサムネールには`button`の役割があります。 サムネールが選択されると、`aria-selected`属性が`true`に設定されます。

スウォッチを表示するコンポーネントには、`listbox`の役割(`aria-label`属性が、そのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています)が割り当てられます。 個々のスウォッチには、セット内のスウォッチの位置を示す役割`option`と`aria-setsize`属性と`aria-posinset`属性があります。 スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`に設定され、`aria-controls`属性が実際のドロップダウンパネル要素を参照するボタンによってアクティブになります。 ドロップダウンパネル自体には、役割`menu`があり、役割`menuitem`を持つサブ要素があります。 各メニュー項目には`aria-label`属性が指定されています。

検索ユーザーインターフェイスは、`search`の役割を持つ要素にグループ化されています。 検索入力フィールドには`searchbox`という役割があり、`SearchPanel.INFO_PROMPT`ローカライゼーション記号で制御される情報ラベルを`aria-describedby`属性で参照します。

モーダルダイアログボックスには`dialog`の役割があります。 ダイアログボックスのヘッダー要素は`aria-labelledby`属性で参照されています。
