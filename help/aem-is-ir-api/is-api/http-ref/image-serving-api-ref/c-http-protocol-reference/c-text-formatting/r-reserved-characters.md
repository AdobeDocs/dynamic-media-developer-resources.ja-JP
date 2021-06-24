---
description: この節では、特定の目的で予約されている文字の一覧を示します。
solution: Experience Manager
title: 予約文字
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 76483f3f-f98b-471d-9c5d-49fa22eaf8a3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 予約文字{#reserved-characters}

この節では、特定の目的で予約されている文字の一覧を示します。

RTFでは、中括弧「`{`」と「`}`」をグループ区切り文字として使用します。 これらはペアで記述する必要があり、ネストできます。 テキスト文字列に中括弧を表示するには、「 `\{` 」と「 `\}` 」を使用します。

>[!NOTE]
>
>RTFで使用するすべての中括弧をURLエンコードする必要があります。

バックスラッシュ「\」は、RTFコマンドやキーワードを導入する際に使用します。 バックスラッシュを表示するには、`'\\'`を使用します。
