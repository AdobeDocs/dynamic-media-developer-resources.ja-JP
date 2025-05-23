---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

ボタンには、役割 `button` と、`aria-label` 属性を持つ説明テキストが設定されています。 属性の値は `aria-label` ボタンのローカリゼーションシンボルの値から入力されます。 ボタンが無効の場合、`aria-disabled` 属性はそれに応じて設定されます。

メインビューにはロール `application` があります。 メインビューの簡単な説明が `aria-roledescription` に提供され、対応するメインビューコンポーネントの `ROLE_DESCRIPTION` のローカリゼーションシンボルによって定義された値が提供されます。 キーボードユーザー向けのナビゲーションヒントは `aria-describedby` を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT` のローカリゼーション記号から取得されます。 アセットの UserData フィールドにラベルが定義されている場合、`aria-label` 属性はそのラベルの値で設定されます。

ホットスポット、地域および画像マップには、役割 `button` と、ホットスポットまたは画像マップのラベルの値を `aria-label` つ属性を持つ説明テキストが設定されています。 ユーザーがホットスポットまたは画像マップにフォーカスを置くと、`aria-describedby` を使用してキーボードユーザーに対するナビゲーションヒントが提供され、使用ヒントのテキストは `USAGE_HINT` のローカライズ記号から得られます。

サムネールの役割は、`ThumbnailGridView.LABEL` のローカリゼーションシンボル `aria-label` よって制御される属性を持つ `dialog` です。 個々のサムネールには役割 `button` があります。 サムネールを選択すると、属性が `true` `aria-selected` 設定されます。

スウォッチを表示するコンポーネントの役割 `listbox` には、`aria-label` の属性がそのコンポーネントの `LABEL` ローカリゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を記述する `aria-setsize` 属性と `aria-posinset` 属性の役割 `option` があります。 スウォッチが選択されている場合は、`aria-selected` 属性が `true` に設定されます。

ドロップダウンリストは、追加の `aria-haspopup` 属性が `true` に設定され、`aria-controls` 属性が実際のドロップダウンパネル要素を参照するボタンによってアクティブ化されます。 ドロップダウンパネル自体には、役割 `menu` があり、その役割 `menuitem` を持つサブ要素があります。 各メニュー項目には、`aria-label` 属性が指定されています。

モーダルダイアログボックスには役割 `dialog` があります。 ダイアログボックスのヘッダー要素は、`aria-labelledby` 属性によって参照されます。
