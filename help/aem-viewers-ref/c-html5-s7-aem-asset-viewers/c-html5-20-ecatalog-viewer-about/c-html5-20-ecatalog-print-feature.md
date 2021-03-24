---
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
title: 印刷機能
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 このボタンをクリックすると、印刷範囲と用紙1枚当たりのページ数を選択できます。

印刷の品質は、`printquality`設定パラメーターを使用して調整できます。 `printquality`をデフォルト値より大幅に高い値に設定することはお勧めしません。 その理由は、クライアントのシステム上のWebブラウザーのメモリ消費が非常に多いからです。 また、Dynamic Mediaクラシック会社に設定されている最大画像応答サイズが、設定されている`printquality`値より大きいことを確認してください。

>[!NOTE]
>
>印刷機能は、デスクトップシステムでのみ使用できます。ただし、Internet Explorer 9は使用できません。

