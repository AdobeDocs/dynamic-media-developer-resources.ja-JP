---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
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

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

トップレベルのビューア要素には役割があります `region` および `aria-label` 属性は、デフォルトでビューアの名前に設定されます。 ラベルは `Container.LABEL` ローカリゼーションシンボル。

ボタンには役割があります `button` と説明テキストセット `aria-label` 属性。 の値 `aria-label` 属性は、ボタンのローカライゼーション記号の値を使用して設定されます。 ボタンが無効な場合、 `aria-disabled` 属性が適切に設定されます。

メインビューには役割があります `application`. メインビューの簡単な説明は、 `aria-roledescription`の値を、 `ROLE_DESCRIPTION` 対応するメインビューコンポーネントのローカライゼーションシンボル。 キーボードユーザーのナビゲーションヒントは、 `aria-describedby`の場合、使用のヒントのテキストは `USAGE_HINT` ローカリゼーションシンボル。 アセットに UserData フィールドで定義されたラベルがある場合、 `aria-label` 属性は、そのようなラベルの値で設定されます。

スウォッチを表示するコンポーネントには、役割があります `listbox` と `aria-label` 属性を `LABEL` そのコンポーネントのローカライゼーションシンボル。 個々のスウォッチには役割があります `option` と `aria-setsize` および `aria-posinset` 属性は、セット内のスウォッチの位置を表します。 スウォッチが選択されている場合、 `aria-selected` 属性を `true`.

スライダーコンポーネントは役割を持ちます `slider` 属性を持つ `aria-valuenow`, `aria-valuemin`、および `aria-valuemax` 現在のスライダ位置を表します。
