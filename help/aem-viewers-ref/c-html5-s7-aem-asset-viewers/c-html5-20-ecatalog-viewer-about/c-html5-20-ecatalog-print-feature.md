---
title: 印刷機能
description: ビューアを使用すると、カタログコンテンツをプリンターに出力できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
TQID: 'https://experienceleague.adobe.com/5eIB7D6O7-d8prjO0MJ9PzUU9TPQe7SZcZAEtznPsv4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# 印刷機能{#print-feature}

ビューアを使用すると、カタログコンテンツをプリンターに出力できます。

印刷機能は、ツールバーの専用ボタンによってトリガーされます。 ボタンをクリックすると、ユーザーは印刷範囲と1枚あたりのページ数を選択できます。

印刷の品質は、`printquality`設定パラメーターを使用して調整できます。 `printquality`を既定値より大きい値に設定することは推奨されません。 その理由は、クライアントのシステム上のweb ブラウザーによるメモリ消費が高くなるためです。 また、Dynamic Media Classic会社に設定された最大画像応答サイズが、設定された`printquality`値よりも大きいことを確認してください。

>[!NOTE]
>
>プリント機能は、Internet Explorer 9を除くデスクトップシステムでのみ使用できます。
