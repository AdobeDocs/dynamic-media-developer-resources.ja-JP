---
description: パスベースのアセットへの直接アクセスを許可します。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

パスベースのアセットへの直接アクセスを許可します。

この属性を定義すると、`include`キーワードと`exclude`キーワードのどちらが使用されるかに応じて、指定したオブジェクトタイプに対してパスベースのアクセスが許可または制限されます。

>[!NOTE]
>
>`AllowDirectAccess`属性を指定しない場合、デフォルト値は`exclude`です。

* `include` は、指定したオブジェクト型に対するアクセスを許可し、その他のすべてのオブジェクトに対するアクセスを制限します。
* `exclude` は、指定したオブジェクトタイプに対するアクセスを制限し、その他すべてに対するアクセスを許可します。

`include`も`exclude`も指定しない場合、`include`と見なされます。

次のタイプを制御できます。

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 例 {#section-4c3765ebaa4245a799b454fc196f9237}

* `IS`および`STATIC`オブジェクトタイプに対してのみ直接アクセスを許可

   `AllowDirectAccess=include:IS,STATIC`

* `IS`と`STATIC``AllowDirectAccess=exclude:IS,STATIC`を除くすべてのオブジェクトタイプに対する直接アクセスを許可

* *no*&#x200B;オブジェクトタイプの直接アクセスを許可する（つまり、noneを含める）

   `AllowDirectAccess=include:`

* *すべての*&#x200B;オブジェクトタイプに対する直接アクセスを許可する（「なし」を除く）

   `AllowDirectAccess=exclude:`

* `include:IS,STATIC`と同じ（`include`/`exclude`が存在しない場合、`include`と見なされます）

   `AllowDirectAccess=IS,STATIC`

   は、この会社で`AllowDirectAccess`属性が指定されていない場合に使用されるデフォルト値です。

* なしを含める（`include:`と同じ）（`include`/`exclude`が存在しない場合、`include`と見なされます）

   `AllowDirectAccess=`
