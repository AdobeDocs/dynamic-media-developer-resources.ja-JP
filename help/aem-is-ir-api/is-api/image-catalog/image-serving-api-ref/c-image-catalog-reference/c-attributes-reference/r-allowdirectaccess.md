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

この属性を定義した場合、指定したオブジェクトタイプに対して、パスベースのアクセスが許可または制限されます。 `include` または `exclude` キーワードが使用されます。

>[!NOTE]
>
>次の場合、 `AllowDirectAccess` 属性が指定されていない場合、デフォルト値は `exclude`.

* `include` は、指定したオブジェクト型に対するアクセスを許可し、その他すべてに対するアクセスを制限します。
* `exclude` は、指定したオブジェクトタイプへのアクセスを制限し、その他すべてに対するアクセスを許可します。

どちらでもない場合 `include` nor `exclude` が指定されている場合、 `include` が想定されます。

以下のタイプを制御できます。

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 次の場合のみ直接アクセスを許可 `IS` および `STATIC` オブジェクトタイプ

  `AllowDirectAccess=include:IS,STATIC`

* 以下を除くすべてのオブジェクトタイプに対する直接アクセスを許可 `IS` および `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 次の直接アクセスを許可： *いいえ* オブジェクトタイプ（なしを含む）

  `AllowDirectAccess=include:`

* 次の直接アクセスを許可： *すべて* オブジェクトのタイプ（「なしを除外」）

  `AllowDirectAccess=exclude:`

* と同等 `include:IS,STATIC` ( `include`/ `exclude` が存在しない。 `include` が想定される場合 )

  `AllowDirectAccess=IS,STATIC`

  はデフォルト値で、 `AllowDirectAccess` この会社の属性が指定されていません。

* なしを含める（と同じ） `include:` ( `include`/ `exclude` が存在しない。 `include` が想定される場合 )

  `AllowDirectAccess=`
