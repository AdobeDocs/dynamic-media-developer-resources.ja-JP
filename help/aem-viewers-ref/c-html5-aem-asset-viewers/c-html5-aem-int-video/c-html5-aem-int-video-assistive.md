---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

ボタンには、役割 `button` と、`aria-label` 属性を持つ説明テキストが設定されています。 属性の値は `aria-label` ボタンのローカリゼーションシンボルの値から入力されます。 ボタンが無効の場合、それに応じ `aria-disabled` 属性が設定されます。

スライダーのコンポーネントには、現在のスライダーの位置を表す属性 `slider`、`aria-valuenow`、`aria-valuemin` を持つ役割 `aria-valuemax` があります。

サムネールの役割は、`dialog` のローカリゼーションシンボル `aria-label` よって制御される属性を持つ `ThumbnailGridView.LABEL` です。 個々のサムネールには役割 `button` があります。 サムネールを選択すると、属性が `aria-selected``true` 設定されます。

スウォッチを表示するコンポーネントの役割 `listbox` には、`aria-label` の属性がそのコンポーネントの `LABEL` ローカリゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を記述する `option` 属性と `aria-setsize` 属性の役割 `aria-posinset` があります。 スウォッチが選択されている場合は、`aria-selected` 属性が `true` に設定されます。

ドロップダウンリストは、追加の `aria-haspopup` 属性が `true` に設定されたボタンと、実際のドロップダウンパネル要素 `aria-controls` 参照する属性によってアクティブ化されます。 ドロップダウンパネル自体には、役割 `menu` があり、その役割 `menuitem` を持つサブ要素があります。 各メニュー項目には、`aria-label` 属性が指定されています。

モーダルダイアログボックスには役割 `dialog` があります。 ダイアログボックスのヘッダー要素は、`aria-labelledby` 属性によって参照されます。
