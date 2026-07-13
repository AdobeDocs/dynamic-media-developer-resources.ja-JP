---
title: 共通のデータタイプ
description: カタログ属性とフィールドには、次のいずれかのタイプのデータを含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 共通のデータタイプ{#common-data-types}

カタログ属性とフィールドには、次のいずれかのタイプのデータを含めることができます。

**カラー**

カラー値。 16進数、パッケージ化されたRGB値、オプションで0xが先行する。 例えば、RGB値`128,255,0`は`0x80ff00`または`80ff00`として指定できます。

**フラグ**

`0`=false、`1`=true、その他の値は不明または未指定を意味します。

**列挙**

`0`は、空のフィールドと同じ、不明または未指定の値を示します。 有効な`enum`値は、1から始まる連続した整数です。

**整数**

符号付き整数値（例：`0, -12, 34`）。 `0`または負の値は特別な意味を持つ可能性があります。

**実数**

符号付き浮動小数点値（例：`0, 12.5, 245 , -2.34e4`）。 0または負の値は特別な意味を持つ場合があります。

**テキスト文字列**

文字列に`<CR>`、`<LF>`、または`<TAB>`文字が含まれていない限り、文字列区切りはオプションです。 区切り文字として、一重引用符と二重引用符のどちらかを使用できます。 引用符を使用する場合、文字列内に埋め込まれたそのような引用符は、連続する2つの引用符を使用してエスケープする必要があります（例：&#39;`This month''s Special`&#39;）。

