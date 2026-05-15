---
description: すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。
solution: Experience Manager
title: 技術サポート
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
TQID: 'https://experienceleague.adobe.com/iaM1o85zC7GNh-RZcMYfjGk99eb8RfobLSGLzwtbOqk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 398
ht-degree: 0%

---

# 技術サポート{#assistive-technology-support}

すべてのビューアーコンポーネントは、ARIA （Accessible Rich Internet Applications）の役割と属性をサポートし、スクリーンリーダーなどの支援テクノロジーとの統合を向上させます。

最上位のビューア要素には、デフォルトでビューアの名前に設定されている役割`region`および`aria-label`属性があります。 ラベルは、`Container.LABEL` ローカライズ記号で制御できます。

ボタンには、役割`button`と`aria-label`属性を持つ記述的なテキストが設定されています。 `aria-label`属性の値は、ボタンのローカライゼーションシンボルの値から入力されます。 ボタンが無効になっている場合、`aria-disabled`属性が適切に設定されます。

メイン ビューには役割`application`があります。 メインビューの簡単な説明は`aria-roledescription`で提供され、対応するメインビューコンポーネントの`ROLE_DESCRIPTION` ローカライゼーションシンボルで定義された値が示されます。 キーボードユーザーのナビゲーションヒントは`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT` ローカライゼーションシンボルから取得されます。 アセットにUserData フィールドで定義されたラベルがある場合、`aria-label`属性にはそのようなラベルの値が設定されます。

ホットスポット、地域、画像マップには、役割`button`と説明テキストが`aria-label`属性で設定され、ホットスポットまたは画像マップのラベルの値が設定されています。 ユーザーがホットスポットまたは画像マップに注目すると、キーボードユーザーのナビゲーションヒントが`aria-describedby`を使用して提供され、使用ヒントのテキストは`USAGE_HINT` ローカライゼーションシンボルから取得されます。

サムネールには、`ThumbnailGridView.LABEL` ローカライゼーションシンボルによって制御される`aria-label`属性を持つ役割`dialog`があります。 個々のサムネールには役割`button`があります。 サムネールを選択すると、`aria-selected`属性が`true`に設定されます。

スウォッチを表示するコンポーネントでは、そのコンポーネントの`LABEL` ローカライゼーションシンボルの値に`aria-label`属性が設定された役割`listbox`が設定されています。 個々のスウォッチには、`aria-setsize`属性と`aria-posinset`属性を持つ役割`option`があり、セット内のスウォッチの位置を表します。 スウォッチを選択すると、`aria-selected`属性が`true`に設定されます。

ドロップダウンリストは、追加の`aria-haspopup`属性が`true`に設定され、実際のドロップダウンパネル要素を参照する`aria-controls`属性が設定されたボタンによってアクティブ化されます。 ドロップダウンパネル自体には、役割`menu`があり、サブエレメントには役割`menuitem`があります。 各メニュー項目には、`aria-label`属性が指定されています。

検索ユーザーインターフェイスは、役割`search`を持つ要素にグループ化されています。 検索入力フィールドには役割`searchbox`があり、`SearchPanel.INFO_PROMPT`のローカライゼーションシンボルによって制御される情報ラベルを`aria-describedby`属性で参照します。

モーダルダイアログボックスの役割は`dialog`です。 ダイアログボックスのヘッダー要素は、`aria-labelledby`属性で参照されています。
