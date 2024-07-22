---
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
title: 印刷機能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 ボタンをクリックすると、ユーザーは印刷範囲と 1 枚あたりのページ数を選択できます。

印刷の品質は、`printquality` 設定パラメーターを使用して調整できます。 `printquality` をデフォルトよりも大幅に高い値に設定することは推奨されません。 理由は、クライアントのシステム上の web ブラウザーによるメモリ消費が非常に多くなるからです。 また、Dynamic Media Classic会社に設定されている画像応答の最大サイズが、設定されている `printquality` 値よりも大きいことを確認してください。

>[!NOTE]
>
>印刷機能は、Internet Explorer 9 以外のデスクトップシステムでのみ使用できます。
