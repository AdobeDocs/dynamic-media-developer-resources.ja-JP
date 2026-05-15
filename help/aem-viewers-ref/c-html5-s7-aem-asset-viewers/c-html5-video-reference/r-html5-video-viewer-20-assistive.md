---
title: 技術サポート
description: すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
TQID: 'https://experienceleague.adobe.com/wOJ59nhF2lMgcT4L8-Qn2PwkVHGYKwTaKR0y1VDtjOY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# 技術サポート{#assistive-technology-support}

すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。

最上位のビューア要素には、デフォルトでビューアの名前に設定されている役割`region`および`aria-label`属性があります。 ラベルは、`Container.LABEL` ローカライズ記号で制御できます。

ボタンには、役割`button`と`aria-label`属性を持つ記述的なテキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーションシンボルの値から入力されます。 ボタンが無効になっている場合、`aria-disabled`属性が適切に設定されます。

スライダーコンポーネントには、現在のスライダーの位置を表す属性`aria-valuenow`、`aria-valuemin`および`aria-valuemax`を持つ役割`slider`があります。

ドロップダウンリストは、実際のドロップダウンパネル要素を参照する`aria-haspopup`属性が`true`および`aria-controls`に設定された追加の属性を持つボタンによってアクティブ化されます。 ドロップダウンパネル自体には役割`menu`があり、サブ要素には役割`menuitem`があります。 各メニュー項目には、`aria-label`属性が指定されています。

モーダルダイアログボックスの役割は`dialog`です。 ダイアログボックスのヘッダー要素は、`aria-labelledby`属性で参照されています。
