---
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
title: 印刷機能
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンでトリガーされます。 ボタンをクリックすると、印刷範囲と用紙1枚あたりのページ数を選択できます。

印刷の品質は、`printquality`設定パラメーターを使用して調整できます。 `printquality`をデフォルトより大きく設定することはお勧めしません。 理由は、クライアントのシステム上のWebブラウザーのメモリ消費が非常に高いからです。 また、Dynamic Media Classicの会社に設定する画像応答の最大サイズが、設定した`printquality`値より大きいことを確認してください。

>[!NOTE]
>
>印刷機能は、Internet Explorer 9を除くデスクトップシステムでのみ使用できます。
