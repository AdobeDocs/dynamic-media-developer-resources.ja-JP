---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位のビューア要素には、初期設定でビ `region` ューアの `aria-label` 名前に設定されている役割と属性があります。 ラベルは、ローカリゼーションシンボルを使用して `Container.LABEL` 制御できます。

ボタンには、役割と、属性を `button` 持つ説明テキストが設定さ `aria-label` れます。 属性の値は、ボ `aria-label` タンのローカリゼーションシンボルの値から設定されます。 ボタンが無効になっている場合は、それ `aria-disabled` に応じて属性が設定されます。

カルーセルスライド間を移動するためのボタンには、現在選択されているスライドに応じて実行時に更新されるラベルが含まれます。 これらのボタンのラベルのテンプレートには、ローカリゼーションシンボルが `CAROUSELVIEWER_TOOLTIP_GOTO` 設定されます。

メインビューにはロールがありま `application`す。 メインビューの簡単な説明は、対応するメインビ `aria-roledescription`ューコンポーネントのローカリゼーションシ `ROLE_DESCRIPTION` ンボルで定義された値と共ににに提供されます。 キーボードユーザーのナビゲーションヒントは、を使 `aria-describedby`用して提供されます。使用ヒントのテキストは、ローカリゼーションシンボル `USAGE_HINT` から取得されます。 アセットにUserDataフィールドで定義されたラベルが含まれている場合、 `aria-label` 属性にはそのラベルの値が設定されます。

ホットスポット、領域および画像マップには、ロールと説明 `button` テキストが設定され、属性が設定さ `aria-label` れ、ホットスポットまたは画像マップのラベルの値が設定されます。 ユーザがホットスポットや画像マップにフォーカスすると、キーボードユーザのナビゲーションヒントが、ローカリゼーションシンボルからの使用 `aria-describedby`ヒントのテキストと共に、を使用して提 `USAGE_HINT` 供されます。
