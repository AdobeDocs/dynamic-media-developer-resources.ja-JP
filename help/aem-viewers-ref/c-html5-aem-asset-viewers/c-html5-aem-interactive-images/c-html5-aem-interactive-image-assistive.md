---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位のビューア要素には、初期設定でビ `region` ューアの `aria-label` 名前に設定されている役割と属性があります。 ラベルは、ローカリゼーションシンボルを使用して `Container.LABEL` 制御できます。

メインビューにはロールがありま `application`す。 メインビューの簡単な説明は、対応するメインビ `aria-roledescription`ューコンポーネントのローカリゼーションシ `ROLE_DESCRIPTION` ンボルで定義された値と共ににに提供されます。 キーボードユーザーのナビゲーションヒントは、を使 `aria-describedby`用して提供されます。使用ヒントのテキストは、ローカリゼーションシンボル `USAGE_HINT` から取得されます。 アセットにUserDataフィールドで定義されたラベルが含まれている場合、 `aria-label` 属性にはそのラベルの値が設定されます。

ホットスポット、領域および画像マップには、ロールと説明 `button` テキストが設定され、属性が設定さ `aria-label` れ、ホットスポットまたは画像マップのラベルの値が設定されます。 ユーザがホットスポットや画像マップにフォーカスすると、キーボードユーザのナビゲーションヒントが、ローカリゼーションシンボルからの使用 `aria-describedby`ヒントのテキストと共に、を使用して提 `USAGE_HINT` 供されます。
