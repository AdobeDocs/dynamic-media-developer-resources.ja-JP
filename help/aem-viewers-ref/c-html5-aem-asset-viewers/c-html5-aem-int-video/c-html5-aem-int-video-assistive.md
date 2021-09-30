---
title: 支援技術のサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性を持つ説明テキストが設定されます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

スライダコンポーネントには、現在のスライダ位置を示す属性`aria-valuenow`、`aria-valuemin`、`aria-valuemax`を持つ役割`slider`があります。

サムネールには、`ThumbnailGridView.LABEL`ローカライゼーションシンボルで制御される`dialog`属性が付いた役割`aria-label`があります。 個々のサムネールには役割`button`があります。 サムネールを選択すると、`aria-selected`属性が`true`に設定されます。

スウォッチを表示するコンポーネントの役割`listbox`は、`aria-label`属性がそのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を表す`option`属性と`aria-setsize`属性が割り当てられています。 `aria-posinset`スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`および`aria-controls`属性に設定されたボタンによってアクティブ化され、実際のドロップダウンパネル要素を参照します。 ドロップダウンパネル自体には、役割`menu`と役割`menuitem`を持つサブ要素があります。 各メニュー項目には、`aria-label`属性が指定されています。

モーダルダイアログボックスには、役割`dialog`があります。 ダイアログボックスのヘッダー要素は`aria-labelledby`属性で参照されます。
