---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、初期設定でビューア名に設定されているロール`region`と`aria-label`の属性があります。 ラベルはローカライゼーション記号`Container.LABEL`で制御できます。

ボタンには、`button`という役割と、`aria-label`属性を持つ説明テキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、`aria-disabled`属性がそれに応じて設定されます。

スライダコンポーネントには、現在のスライダ位置を示す`aria-valuenow`、`aria-valuemin`、`aria-valuemax`という属性を持つロール`slider`があります。

サムネールには、`ThumbnailGridView.LABEL`ローカライゼーション記号で制御される`aria-label`属性を持つ`dialog`ロールがあります。 個々のサムネールには`button`の役割があります。 サムネールが選択されると、`aria-selected`属性が`true`に設定されます。

スウォッチを表示するコンポーネントには、`listbox`の役割(`aria-label`属性が、そのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています)が割り当てられます。 個々のスウォッチには、セット内のスウォッチの位置を示す役割`option`と`aria-setsize`属性と`aria-posinset`属性があります。 スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`および`aria-controls`属性に設定されたボタンによってアクティブになり、実際のドロップダウンパネル要素を参照します。 ドロップダウンパネル自体には、役割`menu`があり、役割`menuitem`を持つサブ要素があります。 各メニュー項目には`aria-label`属性が指定されています。

モーダルダイアログボックスには`dialog`の役割があります。 ダイアログボックスのヘッダー要素は`aria-labelledby`属性で参照されています。
