---
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援技術のサポート
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ，アクセシビリティ
role: Developer,Business Practitioner
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性を持つ説明テキストが設定されます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

スライダコンポーネントには、現在のスライダ位置を示す属性`aria-valuenow`、`aria-valuemin`、`aria-valuemax`を持つ役割`slider`があります。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`および`aria-controls`属性に設定されたボタンによってアクティブ化され、実際のドロップダウンパネル要素を参照します。 ドロップダウンパネル自体には、役割`menu`が割り当てられ、役割`menuitem`を持つサブ要素が割り当てられます。 各メニュー項目には、`aria-label`属性が指定されています。

モーダルダイアログボックスには、役割`dialog`があります。 ダイアログボックスのヘッダー要素は`aria-labelledby`属性で参照されます。
