---
description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-description: すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。
seo-title: 支援テクノロジーのサポート
solution: Experience Manager
title: 支援テクノロジーのサポート
topic: Dynamic media
uuid: 4a84a3a6-e9ba-4511-8228-e1a611f871c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA(Accessible Rich Internet Applications)の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を強化します。

最上位のビューア要素には、初期設定でビ `region` ューアの `aria-label` 名前に設定されている役割と属性があります。 ラベルは、ローカリゼーションシンボルを使用して `Container.LABEL` 制御できます。

ボタンには、役割と、属性を `button` 持つ説明テキストが設定さ `aria-label` れます。 属性の値は、ボ `aria-label` タンのローカリゼーションシンボルの値から設定されます。 ボタンが無効になっている場合は、それ `aria-disabled` に応じて属性が設定されます。

メインビューにはロールがありま `application`す。 メインビューの簡単な説明は、対応するメインビ `aria-roledescription`ューコンポーネントのローカリゼーションシ `ROLE_DESCRIPTION` ンボルで定義された値と共ににに提供されます。 キーボードユーザーのナビゲーションヒントは、を使 `aria-describedby`用して提供されます。使用ヒントのテキストは、ローカリゼーションシンボル `USAGE_HINT` から取得されます。 アセットにUserDataフィールドで定義されたラベルが含まれている場合、 `aria-label` 属性にはそのラベルの値が設定されます。

スウォッチを表示するコンポーネントには、そのコ `listbox` ンポーネ `aria-label` ントのローカリゼーションシンボルの値に設定さ `LABEL` れた属性を持つ役割が割り当てられます。 個々のスウォッチには、セット内のスウォ `option` ッチの `aria-setsize` 位置を示す `aria-posinset` 役割と属性が付いた、およびの属性があります。 スウォッチが選択されている場合は、属性がに設 `aria-selected` 定されていま `true`す。

スライダコンポーネントには、アトリビ `slider` ュート、および現在 `aria-valuenow`のスライダの位 `aria-valuemin``aria-valuemax` 置を示す役割があります。
