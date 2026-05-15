---
description: パスベースのアセットへの直接アクセス。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
TQID: 'https://experienceleague.adobe.com/h2bcjdutPEZID471oI-MWfxG4trg87bIeyAxvoMyKEA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

パスベースのアセットへの直接アクセス。

この属性が定義されている場合、`include`または`exclude` キーワードが使用されているかどうかに応じて、指定されたオブジェクトタイプに対するパスベースのアクセスが許可または制限されます。

>[!NOTE]
>
>`AllowDirectAccess`属性が指定されていない場合、デフォルト値は`exclude`です。

* `include`は、指定されたオブジェクト タイプへのアクセスを許可し、他のすべてのオブジェクト タイプへのアクセスを制限します。
* `exclude`は、指定されたオブジェクトの種類に対するアクセスを制限し、他のすべてのオブジェクトに対するアクセスを許可します。

`include`と`exclude`のどちらも指定しない場合、`include`が想定されます。

次のタイプは制御できます。

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 例 {#section-4c3765ebaa4245a799b454fc196f9237}

* `IS`および`STATIC` オブジェクトタイプに対してのみ直接アクセスを許可する

  `AllowDirectAccess=include:IS,STATIC`

* `IS`と`STATIC``AllowDirectAccess=exclude:IS,STATIC`を除くすべてのオブジェクトタイプに直接アクセスを許可する

* *no* オブジェクトタイプに対する直接アクセスを許可します（つまり、なし）

  `AllowDirectAccess=include:`

* *all* オブジェクトタイプに対する直接アクセスを許可します（つまり、なし除外）

  `AllowDirectAccess=exclude:`

* `include:IS,STATIC`と同等です（`include`/`exclude`が存在しない場合、`include`が想定されます）

  `AllowDirectAccess=IS,STATIC`

  この会社に`AllowDirectAccess`属性が指定されていない場合に使用されるデフォルト値です。

* `include:`と同等のなし（`include`/`exclude`が存在しない場合、`include`が想定されます）

  `AllowDirectAccess=`
