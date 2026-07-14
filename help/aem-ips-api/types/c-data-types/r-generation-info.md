---
description: PostScriptのファイルプロパティ：
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
TQID: 'https://experienceleague.adobe.com/fM-heKQFWRXUn8QWVxJA1yNJ2aqlozRoK5B-ErzamLA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 8%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScriptのファイルプロパティ：

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用される生成エンジン（値については「生成情報」を参照）。 |
| [!DNL originator] | `types:Asset` | 生成で使用されるプライマリアセットのアセットレコード。 |
| [!DNL generated] | `types:Asset` | 生成されたアセットのアセットレコード。 |
| attributeArray | `types:GenerationAttributeArray` | 生成プロセスに関連付けられた属性の配列。 |

