---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位のビューア要素には、初期設定でビ `region` ューアの `aria-label` 名前に設定されている役割と属性があります。 ラベルは、ローカリゼーションシンボルを使用して `Container.LABEL` 制御できます。

ボタンには、役割と、属性を `button` 持つ説明テキストが設定さ `aria-label` れます。 属性の値は、ボ `aria-label` タンのローカリゼーションシンボルの値から設定されます。 ボタンが無効になっている場合は、それに応じ `aria-disabled` て属性が設定されます。

メインビューにはロールがありま `application`す。 メインビューの簡単な説明は、対応するメインビ `aria-roledescription`ューコンポーネントのローカリゼーションシ `ROLE_DESCRIPTION` ンボルで定義された値と共ににに提供されます。 キーボードユーザーのナビゲーションヒントは、を使 `aria-describedby`用して提供されます。使用ヒントのテキストは、ローカリゼーションシンボル `USAGE_HINT` から取得されます。 アセットにUserDataフィールドで定義されたラベルが含まれている場合、 `aria-label` 属性にはそのラベルの値が設定されます。

ホットスポット、領域および画像マップには、ロールと説明 `button` テキストが設定され、属性が設定さ `aria-label` れ、ホットスポットまたは画像マップのラベルの値が設定されます。 ユーザがホットスポットや画像マップにフォーカスすると、キーボードユーザのナビゲーションヒントが、ローカリゼーションシンボルからの使用 `aria-describedby`ヒントのテキストと共に、を使用して提 `USAGE_HINT` 供されます。

サムネールには、ローカリゼーショ `dialog` ンシンボル `aria-label` で制御される属性を持つ `ThumbnailGridView.LABEL` 役割があります。 個々のサムネールには役割があり `button`ます。 サムネールが選択されている場合は、属性がに設 `aria-selected` 定されていま `true`す。

スウォッチを表示するコンポーネントには、そのコ `listbox` ンポーネ `aria-label` ントのローカリゼーションシンボルの値に設定さ `LABEL` れた属性を持つ役割が割り当てられます。 個々のスウォッチには、セット内のスウォ `option` ッチの `aria-setsize` 位置を示す `aria-posinset` 役割と属性が付いた、およびの属性があります。 スウォッチが選択されている場合は、属性がに設 `aria-selected` 定されていま `true`す。

コンボボックスは、追加の属性がに設定され、実際のコンボボ `aria-haspopup` ックス要素を参照 `true` する属 `aria-controls` 性がに設定されたボタンによってアクティブになります。 ドロップダウンパネル自体には、役割を持つサ `menu` ブ要素を持つ役割が割り当てられま `menuitem`す。 各メニュー項目には属性が指定 `aria-label` されています。

モーダルダイアログボックスには役割がありま `dialog`す。 ダイアログボックスのヘッダー要素は、属性によって参照さ `aria-labelledby` れます。
