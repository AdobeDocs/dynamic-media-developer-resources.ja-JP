---
description: アップロードジョブ用の自動セット生成スクリプトリスト。 アップロード用に指定されたすべてのスクリプトが、アップロードされたすべてのアセットに適用されると仮定します。
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# AutoSetCreationOptions{#autosetcreationoptions}

アップロードジョブ用の自動セット生成スクリプトリスト。 アップロード用に指定されたすべてのスクリプトが、アップロードされたすべてのアセットに適用されると仮定します。

構文

## パラメータ {#section-0302e9238dbc4704914e938f42c881e6}

| 名前 | 種類 | 説明 |
|---|---|---|
| autoSetsArray | `types:HandleArray` | の配列 [!DNL PropertySet] は、アップロード時に適用される自動セット生成スクリプトの定義を処理します。 |
