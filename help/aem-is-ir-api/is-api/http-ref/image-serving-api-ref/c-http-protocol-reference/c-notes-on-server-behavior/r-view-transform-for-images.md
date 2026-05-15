---
description: 画像の変形を表示
solution: Experience Manager
title: 画像の変形を表示
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# 画像の変形を表示{#view-transform-for-images}

`req=img` リクエストに応答してクライアントに返された画像は、次の値を考慮して、合成画像から派生されます：`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`、および合成画像のサイズ。

`wid=`と`hei=`が指定されていて、`scl=`が指定されていない場合、合成画像は、`wid=`と`hei=`によって定義されたビュー直方体内に完全に収まるように拡大・縮小されます。 ビュー矩形の縦横比が合成画像の縦横比と異なる場合、拡大/縮小された合成画像は、`align=`値を使用してビュー矩形の中に配置されます（指定されている場合）。指定されていない場合は、中央に配置されます。 画像データでカバーされていないスペースは`bgc=`で埋められます。指定されていない場合は`attribute::BkgColor`で埋められます。

`scl=`が指定されている場合、合成画像はそのスケール係数でスケールされます。 `wid=`または`hei=`が指定されている場合、必要に応じて、拡大・縮小された画像は`wid=`または`hei=`に切り抜かれるか、余分なスペースが追加されます。 `align=`は、画像を切り抜く場所または余分なスペースを追加する場所を指定し、余分なスペースには`bgc=`または`attribute::BkgColor`を入力します。

`wid=`、`hei=`および`scl=`のいずれも指定せず、コンポジット画像の幅または高さが`attribute::DefaultPix`を超える場合、コンポジット画像は`attribute::DefaultPix`を超えないように拡大・縮小されます。 それ以外の場合は、拡大縮小せずに合成画像が使用されます。

これ以上の拡大/縮小を行わずにビュー画像が返されることを保証するには、`scl=1`を指定します。

`rgn=`を指定すると、それに応じて返信画像が切り抜かれ、最終的な返信画像サイズになります。 このサイズは`attribute::MaxPix` （定義されている場合）と比較され、いずれかのディメンションで返信画像が大きい場合はエラーが生成されます。

`fmt=`がアルファなしのデータを指定した場合、返信画像内の透明領域には`bgc=`または`attribute::BkgColor`が入力されます。
