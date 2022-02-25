---
title: 支援テクノロジーのサポート
description: すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 支援テクノロジーのサポート{#assistive-technology-support}

すべてのビューアコンポーネントは、ARIA（アクセシブルなリッチインターネットアプリケーション）の役割と属性をサポートしており、スクリーンリーダーなどの支援テクノロジーとの統合を強化しています。

トップレベルのビューア要素には役割があります `region` および `aria-label` 属性は、デフォルトでビューアの名前に設定されます。 ラベルは `Container.LABEL` ローカリゼーションシンボル。

ボタンには役割があります `button` と、 `aria-label` 属性。 の値 `aria-label` 属性は、ボタンのローカライゼーション記号の値を使用して設定されます。 ボタンが無効な場合、 `aria-disabled` 属性が適切に設定されます。

メインビューには役割があります `application`. メインビューの簡単な説明は、 `aria-roledescription`の値を、 `ROLE_DESCRIPTION` 対応するメインビューコンポーネントのローカライゼーションシンボル。 キーボードユーザーのナビゲーションヒントは、 `aria-describedby`の場合、使用のヒントのテキストは `USAGE_HINT` ローカリゼーションシンボル。 アセットに UserData フィールドで定義されたラベルがある場合、 `aria-label` 属性は、そのようなラベルの値で設定されます。
