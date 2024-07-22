---
title: videoServerUrl
description: Video360 ビューアの URL コマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 76204d0a-449b-4fe5-a2aa-36739fab482f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---

# videoServerUrl{#videoserverurl}

Video360 ビューアの URL コマンド。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオサーバーのルートパス。 ドメインが指定されていない場合、ページの提供元となるドメインが代わりに適用されます。 標準の URI パス解決が適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。 標準的な SaaS の使用には不要です。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```
