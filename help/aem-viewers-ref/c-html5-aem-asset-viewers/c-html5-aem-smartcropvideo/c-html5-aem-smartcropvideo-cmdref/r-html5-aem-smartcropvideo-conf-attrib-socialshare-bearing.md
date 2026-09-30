---
title: SocialShare.bearing
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
TQID: 'https://experienceleague.adobe.com/5b7-Ofn9ZcJTxG-RSwXCbW0pb5EgItA15pG9i2iXUU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%
---
# SocialShare.bearing{#socialshare-bearing}

スマート切り抜きビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタン コンテナのスライド アニメーションの方向を指定します。 </p> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、または<span class="codeph"> right</span>に設定すると、パネルは余分な境界チェックなしで指定された方向にロールアウトされ、外部コンテナによってパネルがクリッピングされる可能性があります。 </p> <p><span class="codeph"> fit-vertical</span>に設定すると、コンポーネントは最初にベースパネルの位置をSocialShareの下部に移動し、そのベースパネルの下部、右側、または左側からロールアウトしようとします。 コンポーネントは、試行のたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、上、右、左の方向にロールアウトを繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定すると、コンポーネントは同様のロジックを使用します。 ただし、最初にベースを右に移動し、右、下、上のロールアウト方向を試してから、左、下、上のロールアウト方向を試してベースを左に移動します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
