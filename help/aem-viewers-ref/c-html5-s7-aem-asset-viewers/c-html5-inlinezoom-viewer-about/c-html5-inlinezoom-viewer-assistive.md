---
title: 技術サポート
description: すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
TQID: 'https://experienceleague.adobe.com/rAaGocul6254eacM2BQ1yHmx3oa3A1RK7UPfalTTZBM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# 技術サポート{#assistive-technology-support}

すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。

最上位のビューア要素には、デフォルトでビューアの名前に設定されている役割`region`および`aria-label`属性があります。 ラベルは、`Container.LABEL` ローカライズ記号で制御できます。

メイン ビューには役割`application`があります。 メインビューの簡単な説明は`aria-roledescription`で提供され、対応するメインビューコンポーネントの`ROLE_DESCRIPTION` ローカライゼーションシンボルで定義された値が示されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT` ローカライゼーションシンボルから取得されます。 アセットにUserData フィールドで定義されたラベルがある場合、`aria-label`属性にはそのようなラベルの値が設定されます。

スウォッチを表示するコンポーネントでは、そのコンポーネントの`LABEL` ローカライゼーションシンボルの値に`aria-label`属性が設定された役割`listbox`が設定されています。 個々のスウォッチには、`aria-setsize`属性と`aria-posinset`属性を持つ役割`option`があり、セット内のスウォッチの位置を表します。 スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。
