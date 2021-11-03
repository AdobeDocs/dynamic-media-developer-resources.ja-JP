---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

トップレベルのビューア要素には役割があります `region` および `aria-label` 属性は、デフォルトでビューアの名前に設定されます。 ラベルは `Container.LABEL` ローカリゼーションシンボル。

ボタンには役割があります `button` と説明テキストセット `aria-label` 属性。 の値 `aria-label` 属性は、ボタンのローカライゼーション記号の値を使用して設定されます。 ボタンが無効な場合、 `aria-disabled` 属性が適切に設定されます。

スライダーコンポーネントは役割を持ちます `slider` 属性を持つ `aria-valuenow`, `aria-valuemin`、および `aria-valuemax` 現在のスライダ位置を表します。

ドロップダウンリストは、追加の `aria-haspopup` 属性を `true` および `aria-controls` 実際のドロップダウンパネル要素を参照する属性。 ドロップダウンパネル自体には、の役割があります `menu` 役割を持つサブ要素を持つ `menuitem`. 各メニュー項目には、 `aria-label` 属性が指定されました。

モーダルダイアログボックスには役割があります `dialog`. このダイアログボックスのヘッダー要素は、 `aria-labelledby` 属性。
