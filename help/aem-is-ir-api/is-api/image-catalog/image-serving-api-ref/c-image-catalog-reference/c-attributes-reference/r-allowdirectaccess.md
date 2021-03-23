---
description: パスベースのアセットへの直接アクセスを許可します。
seo-description: パスベースのアセットへの直接アクセスを許可します。
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

パスベースのアセットへの直接アクセスを許可します。

この属性を定義すると、`include`キーワードと`exclude`キーワードのどちらが使用されるかに応じて、指定したオブジェクトタイプに対してパスベースのアクセスが許可または制限されます。

>[!NOTE]
>
>`AllowDirectAccess`属性を指定しない場合のデフォルト値は`exclude`です。

* `include` 指定したオブジェクトタイプへのアクセスを許可し、その他のすべてのオブジェクトのアクセスを制限します。
* `exclude` 指定したオブジェクトタイプへのアクセスが制限され、その他のすべてのオブジェクトに対するアクセスが許可されます。

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

* `IS`および`STATIC`オブジェクトタイプでのみ直接アクセスを許可

   `AllowDirectAccess=include:IS,STATIC`

* `IS`と`STATIC``AllowDirectAccess=exclude:IS,STATIC`を除くすべてのオブジェクトタイプで直接アクセスを許可する

* **&#x200B;オブジェクトタイプのへの直接アクセスを許可する（つまり、何も含めない）

   `AllowDirectAccess=include:`

* *すべての*&#x200B;オブジェクトタイプに対する直接アクセスを許可する（つまり、「なしを除外」）

   `AllowDirectAccess=exclude:`

* `include:IS,STATIC`と同等（`include`/ `exclude`が存在しない場合、`include`と解釈されます）

   `AllowDirectAccess=IS,STATIC`

   この会社に`AllowDirectAccess`属性が指定されていない場合は、これがデフォルト値になります。

* なし（`include:`と同じ）（`include`/ `exclude`が存在しない場合は`include`と見なされます）

   `AllowDirectAccess=`

