---
title: 技術サポート
description: すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
TQID: 'https://experienceleague.adobe.com/G19CyChLIW5c9aK-ZGnUBRQtSB31YY7nK0Ia90WwaDc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 0%

---

# 技術サポート{#assistive-technology-support}

すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。

最上位のビューア要素には、デフォルトでビューアの名前に設定されている役割`region`および`aria-label`属性があります。 ラベルは、`Container.LABEL` ローカライズ記号で制御できます。

メイン ビューには役割`application`があります。 メインビューの簡単な説明は`aria-roledescription`で提供され、対応するメインビューコンポーネントの`ROLE_DESCRIPTION` ローカライゼーションシンボルで定義された値が示されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT` ローカライゼーションシンボルから取得されます。 アセットにUserData フィールドで定義されたラベルがある場合、`aria-label`属性にはそのようなラベルの値が設定されます。

ホットスポット、地域、画像マップには、役割`button`と説明テキストが`aria-label`属性で設定され、ホットスポットまたは画像マップのラベルの値が設定されています。 ユーザーがホットスポットまたは画像マップに注目すると、キーボードユーザーのナビゲーションヒントが`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT` ローカライゼーションシンボルから取得されます。
