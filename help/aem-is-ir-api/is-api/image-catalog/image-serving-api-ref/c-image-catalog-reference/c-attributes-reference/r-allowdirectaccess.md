---
description: パスベースのアセットへの直接アクセスを許可します。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

パスベースのアセットへの直接アクセスを許可します。

この属性を定義した場合、`include` キーワードと `exclude` キーワードのどちらが使用されているかに応じて、指定したオブジェクトタイプに対するパスベースのアクセスが許可または制限されます。

>[!NOTE]
>
>`AllowDirectAccess` 属性を指定しない場合、デフォルト値は `exclude` です。

* `include` は、指定したオブジェクトタイプへのアクセスを許可し、その他すべてのタイプへのアクセスを制限します。
* `exclude` は、指定したオブジェクトタイプのアクセスを制限し、その他すべてのオブジェクトタイプのアクセスを許可します。

`include` も `exclude` も指定されていない場合、`include` が想定されます。

次のタイプを制御できます。

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 例 {#section-4c3765ebaa4245a799b454fc196f9237}

* `IS` および `STATIC` オブジェクト タイプに対してのみ直接アクセスを許可する

  `AllowDirectAccess=include:IS,STATIC`

* `IS` および `STATIC` `AllowDirectAccess=exclude:IS,STATIC` を除くすべてのオブジェクトタイプに直接アクセスを許可する

* *いいえ* オブジェクトタイプへの直接アクセスを許可する（つまり、なしを含める）

  `AllowDirectAccess=include:`

* *すべて* オブジェクトタイプに直接アクセスを許可（つまり、なしを除外）

  `AllowDirectAccess=exclude:`

* `include:IS,STATIC` と同等です（`include`/ `exclude` が存在しない場合、`include` が想定されます）

  `AllowDirectAccess=IS,STATIC`

  なお、は、この会社に `AllowDirectAccess` 属性が指定されていない場合に使用されるデフォルト値です。

* 何も含まない、`include:` と同等（`include`/ `exclude` が存在しない場合、`include` が想定されます）

  `AllowDirectAccess=`
