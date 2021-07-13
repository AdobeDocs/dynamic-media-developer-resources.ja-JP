---
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
solution: Experience Manager
title: 支援技術のサポート
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索，アクセシビリティ
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 支援技術のサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位レベルのビューア要素には、デフォルトでビューア名に設定されている役割`region`と`aria-label`属性があります。 ラベルは`Container.LABEL`ローカリゼーション記号で制御できます。

ボタンには、役割`button`と、`aria-label`属性で設定された説明テキストが含まれます。 `aria-label`属性の値は、ボタンのローカライゼーション記号の値から設定されます。 ボタンが無効になると、それに応じて`aria-disabled`属性が設定されます。

メインビューには役割`application`があります。 メインビューの簡単な説明は、 `aria-roledescription`に、対応するメインビューコンポーネントの`ROLE_DESCRIPTION`ローカライゼーション記号で定義された値と共に提供されます。 キーボードユーザーのナビゲーションヒントは、`aria-describedby`を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT`ローカライゼーション記号から取得されます。 アセットのUserDataフィールドにラベルが定義されている場合、`aria-label`属性にはそのラベルの値が設定されます。

ホットスポット、領域、および画像マップには、役割`button`と`aria-label`属性で設定された説明テキストが割り当てられ、ホットスポットまたは画像マップラベルの値が割り当てられます。 ユーザーがホットスポットや画像マップにフォーカスを置くと、キーボードユーザーのナビゲーションヒントが`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT`ローカライゼーションシンボルから取得されます。

サムネールには、`ThumbnailGridView.LABEL`ローカライゼーションシンボルで制御される`dialog`属性が付いた役割`aria-label`があります。 個々のサムネールには役割`button`があります。 サムネールを選択すると、`aria-selected`属性が`true`に設定されます。

スウォッチを表示するコンポーネントの役割`listbox`は、`aria-label`属性がそのコンポーネントの`LABEL`ローカライゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を表す`option`属性と`aria-setsize`属性が割り当てられています。 `aria-posinset`スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`に設定されたボタンと、実際のドロップダウンパネル要素を参照する`aria-controls`属性を持つボタンによってアクティブ化されます。 ドロップダウンパネル自体には、役割`menu`が割り当てられ、役割`menuitem`を持つサブ要素が割り当てられます。 各メニュー項目には、`aria-label`属性が指定されています。

検索ユーザーインターフェイスは、役割`search`を持つ要素内にグループ化されます。 検索入力フィールドは役割`searchbox`を持ち、`aria-describedby`属性を持つ`SearchPanel.INFO_PROMPT`ローカリゼーションシンボルによって制御される情報ラベルを参照します。

モーダルダイアログボックスには、役割`dialog`があります。 ダイアログボックスのヘッダー要素は`aria-labelledby`属性で参照されます。
