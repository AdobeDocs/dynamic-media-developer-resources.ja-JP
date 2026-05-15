---
title: 互換性に関するメモ
description: オペレーティングシステム、ブラウザー、モバイルデバイスの互換性に関するメモ。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
autotag-review: '2026-05-13T21:03:11.123Z'
TQID: 'https://experienceleague.adobe.com/4iK-oLqDVtdeWfreRttUqRBBNOf6nTftLhmYnKtj08w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 422
ht-degree: 0%

---

# 互換性に関するメモ{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザー、モバイルデバイスの互換性に関するメモ。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとの互換性がありません。 アダプティブビデオセットを再アップロードして、再生を許可します。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側の拡大・縮小では、ユーザーがページにズームインすると、UIと画像がぼやけます。 ユーザーインターフェイスのフォーマットも、ズームに応じて誤って表示され、全画面に引き継がれます。
* モバイルデバイスのサイズ制限により、Mixed Media Viewerでは、埋め込みスウォッチ コンポーネントをタップする代わりに、埋め込み画像セットのフレームを入れ替えるためにスライドジェスチャーを使用します。 コンポーネントは視覚的なインジケーターとしてあります。
* Internet Explorerのブラウザーと一部のタッチデバイスでは、フルスクリーンモードはデバイス画面全体を占有しません。 代わりに、アプリケーションのサイズをブラウザーウィンドウのサイズに変更します。
* 「閉じる」ボタンは、iOS 8.0およびiOS 8.1では機能しませんが、iOS 8.2では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* ZoomおよびeCatalog ビューアでメモリリークが発生しました。 フレームを通してナビゲーションを繰り返すと、ブラウザーがクラッシュします。
* ビューアをダブルタップすると、ブラウザーサイドの拡大・縮小が有効になっているビューアの代わりに、ページ全体が拡大・縮小されます。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* ブラウザーの設定で全画面表示がオンになっているポートレートモードで、デバイスがタブレットとして検出されました。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアをダブルタップすると、ブラウザーサイドの拡大・縮小が有効になっている状態で、ページ全体がビューアではなくズームされます。

## Galaxy Nexus 10とGalaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalogでは、ページのスプレッドが正しくなく、縦方向と横方向が表示されます。

## HTC モバイルデバイス {#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできない場合は、HTC UI ラッパー（HTC Sense）の「機能」です。 この機能は、ビューアで「ピンチでズーム」ジェスチャーを使用すると、ページ全体がズームされる可能性があります。 代わりに、ダブルタップジェスチャーを使用します。
* 画像マップが小さく近い場合は、画像マップアイコンが重なります。

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate`修飾子は、ソフトウェア HLSおよびFlash HDSの再生でのみサポートされています。 再生がネイティブプレーヤーを使用している場合は機能しません。
* OGGおよびWebM プログレッシブ再生はサポートされていません。
* ブラウザーの拡大・縮小によって、ビデオプレーヤーが正しくないサイズで表示される（Windows®Campaign コントロールパネルの表示設定を含む）。
* SafariでHLS ストリーミングを使用しているビデオのシークに一貫性がありません。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks モードはサポートされていません。
* 互換性モードはサポートされていません。
* モバイル版のInternet Explorerはサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大きなeCatalogsを使用すると、iPad 2でブラウザーがクラッシュします。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1以降：インターネットプラグインの設定により、Flash ビデオの再生が禁止されています。
* SafariでHLS ストリーミングを使用しているビデオのシークに一貫性がありません。
* HLS ストリーミングを使用してSafari 6でビデオの終了を求めることができません。
