---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 52f5dad9-7309-4385-99bc-79d02d3ba2d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位のビューア要素には、初期設定でビ `region` ューアの `aria-label` 名前に設定されている役割と属性があります。 ラベルは、ローカリゼーションシンボルを使用して `Container.LABEL` 制御できます。

ボタンには、役割と、属性を `button` 持つ説明テキストが設定さ `aria-label` れます。 属性の値は、ボ `aria-label` タンのローカリゼーションシンボルの値から設定されます。 ボタンが無効になっている場合は、それ `aria-disabled` に応じて属性が設定されます。

スライダコンポーネントには、アトリビ `slider` ュート、および現在 `aria-valuenow`のスライダの位 `aria-valuemin``aria-valuemax` 置を示す役割があります。

コンボボックスは、実際のコンボボックス要素を参照する属性と、 `aria-haspopup` に追加の属性が設定さ `true` れたボ `aria-controls` タンによってアクティブになります。 ドロップダウンパネル自体には、役割を持つサ `menu` ブ要素を持つ役割が割り当てられま `menuitem`す。 各メニュー項目には属性が指定 `aria-label` されています。

モーダルダイアログボックスには役割がありま `dialog`す。 ダイアログボックスのヘッダー要素は、属性によって参照さ `aria-labelledby` れます。
