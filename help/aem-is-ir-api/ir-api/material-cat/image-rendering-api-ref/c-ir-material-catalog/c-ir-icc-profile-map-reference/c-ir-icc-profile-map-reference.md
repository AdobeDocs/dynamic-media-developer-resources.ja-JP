---
description: 画像カタログに ICC プロファイルマップが必要な場合は、属性 IccProfileMapFile にプロファイルマップファイルの相対パスまたは絶対パスを指定する必要があります。
solution: Experience Manager
title: ICC プロファイルマップ参照
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c90a1fa-fa38-4d20-9694-1654ac9690e2
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# ICC プロファイルマップ参照{#icc-profile-map-reference}

画像カタログに ICC プロファイルマップが必要な場合は、プロファイルマップファイルの相対パスまたは絶対パスを attribute::IccProfileMapFile で指定する必要があります。

特定の材料カタログの ICC プロファイルマップのエントリは、デフォルトカタログの ICC プロファイルマップのエントリを上書きします。

画像レンダリングでは、ICC 仕様に準拠したカラープロファイルファイルをサポートしています。
