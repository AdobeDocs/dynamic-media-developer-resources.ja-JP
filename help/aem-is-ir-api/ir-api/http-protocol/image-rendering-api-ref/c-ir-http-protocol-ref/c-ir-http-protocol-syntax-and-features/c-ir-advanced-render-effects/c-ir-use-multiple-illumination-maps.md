---
description: 一部のアプリケーションでは、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。
solution: Experience Manager
title: 複数のイルミネーションマップの使用
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 複数のイルミネーションマップの使用{#using-multiple-illumination-maps}

一部のアプリケーションでは、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。

各ビネットに対して最大3つの照明マップを作成できます。 レンダリング操作のイルミネーションマップは、 `illum=`コマンドまたは`gloss=`コマンドを使用して選択されます。

**デフォ** ルトの選択 `illum=` もも `gloss=` 指定しない場合、レンダラーは最初に作成した照明マップ（通常はマップA、「フラット」照明マップ）を使用します。

**[自動選`gloss=`** 択]を指定しな `illum=` い場合、または —1に設定した場合、レンダラーは指定した値とビネット内の各照明マップに関連付けられた光沢値を比較 `gloss=` し、指定した値に最も光沢値が近い照明マップを選択しま `gloss=`す。

**を使用した明示的`illum=`** な選 `illum=` 択を指定し、0、1、または2に設定した場合、レンダラーは対応するイルミネーションマップを使用します。 `gloss=` は、イルミネーションマップを選択する目的で無視されます。

ビネットに1つのイルミネーションマップのみが含まれる場合、レンダラーはそのマップを使用し、 `illum=`および`gloss=`コマンドは無視します。
