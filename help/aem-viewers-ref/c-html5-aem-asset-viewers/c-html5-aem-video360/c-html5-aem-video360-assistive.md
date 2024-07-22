---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

ボタンには、役割 `button` と、`aria-label` 属性を持つ説明テキストが設定されています。 属性の値は `aria-label` ボタンのローカリゼーションシンボルの値から入力されます。 ボタンが無効の場合、それに応じ `aria-disabled` 属性が設定されます。

スライダーのコンポーネントには、現在のスライダーの位置を表す属性 `aria-valuenow`、`aria-valuemin`、`aria-valuemax` を持つ役割 `slider` があります。

ドロップダウンリストは、追加の `aria-haspopup` 属性が `true` に設定されたボタンと、実際のドロップダウンパネル要素 `aria-controls` 参照する属性によってアクティブ化されます。 ドロップダウンパネル自体には、役割 `menu` があり、その役割 `menuitem` を持つサブ要素があります。 各メニュー項目には、`aria-label` 属性が指定されています。

モーダルダイアログボックスには役割 `dialog` があります。 ダイアログボックスのヘッダー要素は、`aria-labelledby` 属性によって参照されます。
