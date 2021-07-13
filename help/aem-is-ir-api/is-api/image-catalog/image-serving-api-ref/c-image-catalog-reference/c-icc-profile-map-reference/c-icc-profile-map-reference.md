---
description: 画像カタログにICCプロファイルマップが必要な場合は、プロファイルマップファイルの相対パスまたは絶対パスを属性IccProfileMapFileで指定する必要があります。
solution: Experience Manager
title: ICCプロファイルマップのリファレンス
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f6b75a15-55b4-44e7-a409-2eaed4e752c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# ICCプロファイルマップのリファレンス{#icc-profile-map-reference}

画像カタログにICCプロファイルマップが必要な場合は、プロファイルマップファイルの相対パスまたは絶対パスをattribute::IccProfileMapFileで指定する必要があります。

特定の画像カタログのICCプロファイルマップ内のエントリは、デフォルトカタログのICCプロファイルマップ内のエントリを上書きします。

画像サービングは、ICC仕様を満たすカラープロファイルファイルをサポートします。
