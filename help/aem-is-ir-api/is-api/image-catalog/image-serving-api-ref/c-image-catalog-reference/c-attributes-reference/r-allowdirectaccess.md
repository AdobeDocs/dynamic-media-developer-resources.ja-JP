---
description: パスベースのアセットへの直接アクセスを許可します。
seo-description: パスベースのアセットへの直接アクセスを許可します。
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

パスベースのアセットへの直接アクセスを許可します。

この属性を定義すると、パスベースのアクセスは、キーワードとキーワードのどちらが使用されているかに応じて、指定したオブジェクトタイプに対して許 `include` 可また `exclude` は制限されます。

>[!NOTE]
>
>属性が指 `AllowDirectAccess` 定されていない場合、デフォルト値はで `exclude`す。

* `include` 指定したオブジェクトタイプへのアクセスを許可し、その他のすべてのオブジェクトのアクセスを制限します。
* `exclude` は、指定したオブジェクトタイプへのアクセスを制限し、その他のすべてのオブジェクトに対するアクセスを許可します。

も指定され `include` ていな `exclude` い場合は、が `include` 想定されます。

次のタイプを制御できます。

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 例 {#section-4c3765ebaa4245a799b454fc196f9237}

* およびオブジェクトタイプに対してのみ直接 `IS` アクセス `STATIC` を許可する

   `AllowDirectAccess=include:IS,STATIC`

* とを除くすべてのオブジェクトタイプに対して直接アクセスを許可 `IS` する `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* オブジェクトタイプ *なし* （つまり、「なし」を含む）の直接アクセスを許可

   `AllowDirectAccess=include:`

* すべてのオブジェクトタ *イプ* （「なしを除外」など）に対する直接アクセスを許可

   `AllowDirectAccess=exclude:`

* 等価( `include:IS,STATIC` /がな `include`い場合は、 `exclude``include` と見なされます)

   `AllowDirectAccess=IS,STATIC`

   これは、この会社に属性が指定されていない場合 `AllowDirectAccess` に使用されるデフォルト値です。

* 「なし」を含める( `include:` と同じ)( `include`/が存在 `exclude` しない場合、と見な `include` されます)

   `AllowDirectAccess=`

