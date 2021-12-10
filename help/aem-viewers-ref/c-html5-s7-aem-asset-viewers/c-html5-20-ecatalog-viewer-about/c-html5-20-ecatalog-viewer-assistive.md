---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

トップレベルのビューア要素には役割があります `region` および `aria-label` 属性は、デフォルトでビューアの名前に設定されます。 ラベルは `Container.LABEL` ローカリゼーションシンボル。

ボタンには役割があります `button` と、 `aria-label` 属性。 の値 `aria-label` 属性は、ボタンのローカライゼーション記号の値を使用して設定されます。 ボタンが無効な場合、 `aria-disabled` 属性が適切に設定されます。

メインビューには役割があります `application`. メインビューの簡単な説明は、 `aria-roledescription`の値を、 `ROLE_DESCRIPTION` 対応するメインビューコンポーネントのローカライゼーションシンボル。 キーボードユーザーのナビゲーションヒントは、 `aria-describedby`の場合、使用のヒントのテキストは `USAGE_HINT` ローカリゼーションシンボル。 アセットに UserData フィールドで定義されたラベルがある場合、 `aria-label` 属性は、そのようなラベルの値で設定されます。

ホットスポット、領域、画像マップは、役割を持ちます `button` と説明テキストセット `aria-label` 属性の値を指定します。 ユーザーがホットスポットまたは画像マップにフォーカスを置くと、キーボードユーザーのナビゲーションヒントが、 `aria-describedby`( 使用のヒントのテキストを `USAGE_HINT` ローカリゼーションシンボル。

サムネールには役割があります `dialog` と `aria-label` 属性 `ThumbnailGridView.LABEL` ローカリゼーションシンボル。 個々のサムネールには役割があります `button`. サムネールを選択した場合は、 `aria-selected` 属性を `true`.

スウォッチを表示するコンポーネントには、役割があります `listbox` と `aria-label` 属性を `LABEL` そのコンポーネントのローカライゼーションシンボル。 個々のスウォッチには役割があります `option` と `aria-setsize` および `aria-posinset` 属性は、セット内のスウォッチの位置を表します。 スウォッチが選択されている場合、 `aria-selected` 属性を `true`.

ドロップダウンリストは、追加の `aria-haspopup` 属性を `true` そして `aria-controls` 実際のドロップダウンパネル要素を参照する属性。 ドロップダウンパネル自体には、の役割があります `menu` 役割を持つサブ要素を持つ `menuitem`. 各メニュー項目には、 `aria-label` 属性が指定されました。

モーダルダイアログボックスには役割があります `dialog`. このダイアログボックスのヘッダー要素は、 `aria-labelledby` 属性。
