---
title: 支援技術のサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

トップレベルのビューア要素には、デフォルトでビューアの名前に設定された役割 `region` と `aria-label` 属性があります。 ラベルは `Container.LABEL` ローカリゼーション記号で制御できます。

ボタンには、`button` と `aria-label` 属性で設定された説明テキストが含まれます。 `aria-label` 属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて `aria-disabled` 属性が設定されます。

スライダコンポーネントには、現在のスライダ位置を示す `aria-valuenow`、`aria-valuemin`、および `aria-valuemax` 属性を持つ役割 `slider` があります。

コンボボックスは、追加の `aria-haspopup` 属性が `true` および `aria-controls` 属性に設定されたボタンによってアクティブ化され、実際のドロップダウンパネル要素を参照します。 ドロップダウンパネル自体には、役割 `menu` があり、役割 `menuitem` を持つサブ要素があります。 各メニュー項目には、`aria-label` 属性が指定されています。

モーダルダイアログボックスには、役割 `dialog` が割り当てられます。 ダイアログボックスのヘッダー要素は `aria-labelledby` 属性で参照されます。
