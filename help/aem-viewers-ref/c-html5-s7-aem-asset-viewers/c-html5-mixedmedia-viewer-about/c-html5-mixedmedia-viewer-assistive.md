---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets,Accessibility
role: Developer,User
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

ボタンには、役割 `button` と、`aria-label` 属性を持つ説明テキストが設定されています。 属性の値は `aria-label` ボタンのローカリゼーションシンボルの値から入力されます。 ボタンが無効の場合、それに応じ `aria-disabled` 属性が設定されます。

メインビューにはロール `application` があります。 メインビューの簡単な説明が `aria-roledescription` に提供され、対応するメインビューコンポーネントの `ROLE_DESCRIPTION` のローカリゼーションシンボルによって定義された値が提供されます。 キーボードユーザー向けのナビゲーションヒントは `aria-describedby` を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT` のローカリゼーション記号から取得されます。 アセットの UserData フィールドにラベルが定義されている場合、`aria-label` 属性はそのラベルの値で設定されます。

スウォッチを表示するコンポーネントの役割 `listbox` には、`aria-label` の属性がそのコンポーネントの `LABEL` ローカリゼーションシンボルの値に設定されています。 個々のスウォッチには、セット内のスウォッチの位置を記述する `aria-setsize` 属性と `aria-posinset` 属性の役割 `option` があります。 スウォッチが選択されている場合は、`aria-selected` 属性が `true` に設定されます。

スライダーのコンポーネントには、現在のスライダーの位置を表す属性 `aria-valuenow`、`aria-valuemin`、`aria-valuemax` を持つ役割 `slider` があります。
