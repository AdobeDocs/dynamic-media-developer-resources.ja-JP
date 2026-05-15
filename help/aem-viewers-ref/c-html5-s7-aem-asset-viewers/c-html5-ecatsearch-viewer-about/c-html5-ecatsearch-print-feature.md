---
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
title: 印刷機能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 ボタンをクリックすると、ユーザーは印刷範囲と1枚あたりのページ数を選択できます。

印刷の品質は、`printquality`設定パラメーターを使用して調整できます。 `printquality`をデフォルトよりも大幅に高い値に設定することは推奨されません。 その理由は、クライアントのシステム上のweb ブラウザーによるメモリの消費量が非常に高くなるためです。 また、Dynamic Media Classic会社に設定された最大画像応答サイズが、設定された`printquality`値よりも大きいことを確認してください。

>[!NOTE]
>
>プリント機能は、Internet Explorer 9を除くデスクトップシステムでのみ使用できます。
