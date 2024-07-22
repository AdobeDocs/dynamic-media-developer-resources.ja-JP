---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントでは、ARIA （アクセシブルリッチインターネットアプリケーション）の役割と属性をサポートして、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

最上位のビューア要素にはロール `region` があり、`aria-label` の属性はデフォルトでビューアの名前に設定されています。 `Container.LABEL` のローカリゼーションシンボルを使用してラベルを制御できます。

ボタンには、役割 `button` と、`aria-label` 属性を持つ説明テキストが設定されています。 属性の値は `aria-label` ボタンのローカリゼーションシンボルの値から入力されます。 ボタンが無効の場合、それに応じ `aria-disabled` 属性が設定されます。

カルーセルスライド内を移動できるボタンには、現在選択しているスライドに応じて、実行時に更新されるラベルが付いています。 これらのボタンのラベルのテンプレートは、ローカリゼーションシンボル `CAROUSELVIEWER_TOOLTIP_GOTO` 設定されています。

メインビューにはロール `application` があります。 メインビューの簡単な説明が `aria-roledescription` に提供され、対応するメインビューコンポーネントの `ROLE_DESCRIPTION` のローカリゼーションシンボルによって定義された値が提供されます。 キーボードユーザー向けのナビゲーションヒントは `aria-describedby` を使用して提供されます。使用ヒントのテキストは、`USAGE_HINT` のローカリゼーション記号から取得されます。 アセットの UserData フィールドにラベルが定義されている場合、`aria-label` 属性はそのラベルの値で設定されます。

ホットスポット、地域および画像マップには、役割 `button` と、ホットスポットまたは画像マップのラベルの値を `aria-label` つ属性を持つ説明テキストが設定されています。 ユーザーがホットスポットまたは画像マップにフォーカスを置くと、`aria-describedby` を使用してキーボードユーザーに対するナビゲーションヒントが提供され、使用ヒントのテキストは `USAGE_HINT` のローカライズ記号から得られます。
