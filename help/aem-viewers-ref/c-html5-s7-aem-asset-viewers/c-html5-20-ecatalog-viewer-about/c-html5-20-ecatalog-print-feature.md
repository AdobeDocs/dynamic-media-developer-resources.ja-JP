---
title: 印刷機能
description: ビューアを使用すると、カタログコンテンツをプリンタに出力できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンタに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 このボタンをクリックすると、印刷範囲と 1 シートあたりのページ数を選択できます。

印刷の品質は、 `printquality` 設定パラメーター。 設定 `printquality` をデフォルトより大きい値に設定することはお勧めしません。 これは、クライアントのシステム上の Web ブラウザーのメモリ消費が高くなるからです。 また、Dynamic Media Classicの会社に設定されている最大画像応答サイズが、設定済みの画像応答サイズよりも大きいことを確認してください `printquality` の値です。

>[!NOTE]
>
>印刷機能は、Internet Explorer 9 を除くデスクトップシステムでのみ使用できます。
