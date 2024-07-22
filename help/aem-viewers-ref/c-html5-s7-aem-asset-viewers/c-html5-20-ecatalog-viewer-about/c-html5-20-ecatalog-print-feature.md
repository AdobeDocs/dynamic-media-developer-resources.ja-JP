---
title: 印刷機能
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 ボタンをクリックすると、ユーザーは印刷範囲と 1 枚あたりのページ数を選択できます。

印刷の品質は、`printquality` 設定パラメーターを使用して調整できます。 `printquality` をデフォルトより大きい値に設定することは推奨されません。 クライアントのシステム上の web ブラウザーによるメモリ消費が多くなるからです。 また、Dynamic Media Classic会社に設定されている画像応答の最大サイズが、設定されている `printquality` 値よりも大きいことを確認してください。

>[!NOTE]
>
>印刷機能は、Internet Explorer 9 以外のデスクトップシステムでのみ使用できます。
