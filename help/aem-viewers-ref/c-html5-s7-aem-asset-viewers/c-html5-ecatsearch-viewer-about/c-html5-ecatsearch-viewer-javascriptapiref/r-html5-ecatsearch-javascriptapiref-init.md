---
title: init
description: eCatalog Viewer用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
TQID: 'https://experienceleague.adobe.com/Hb-C6aORHF8--oX3IqgRZIi1rfbLg39F0Ewzb4sg45U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 1%

---

# init{#init}

eCatalog Viewer用JavaScript API リファレンス。

[!DNL `init()`]

eCatalog Viewerの初期化を開始します。 この時点では、ビューアコードがIDで見つけられるように、コンテナ DOM要素を作成する必要があります。

コンテナ要素がまだweb ページレイアウトの一部ではない場合（例えば、割り当てられた[!DNL `display:none`] スタイルを使用して非表示にできる場合など）、ビューアは初期化プロセスを中断します。 web ページがコンテナ要素をレイアウトに戻すまで行われます。 このイベントが発生すると、ビューアの読み込みが自動的に再開されます。

ビューアのライフサイクル中に、このメソッドを1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

