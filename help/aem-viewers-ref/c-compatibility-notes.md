---
description: オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関する注意事項。
solution: Experience Manager
title: 互換性に関する注意
feature: Dynamic Mediaクラシック，ビューア，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 互換性に関する注意{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関する注意事項。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとは互換性がありません。 アダプティブビデオセットを再アップロードして再生を許可します。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側での拡大/縮小により、ユーザーがページにズームインすると、UIと画像がぼやけます。 また、ズームに応じてユーザインターフェイスの形式も正しく表示されず、フルスクリーンに表示されます。
* モバイルデバイスのサイズ制限により、混在メディアビューアでは、埋め込みのスウォッチコンポーネントをタップする代わりに、スライドジェスチャを使用して埋め込み画像セット内のフレームを入れ替えます。 コンポーネントは視覚的なインジケーターとして存在します。
* Internet Explorerブラウザーおよび一部のタッチデバイスでは、フルスクリーンモードではデバイス画面全体が表示されません。 代わりに、ブラウザーウィンドウのサイズに合わせてアプリケーションのサイズが変更されます。
* 閉じるボタンはiOS 8.0およびiOS 8.1では機能しませんが、iOS 8.2では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* ズームビューアおよびeCatalogビューアでメモリリークが見られます。 フレーム間を繰り返しナビゲーションすると、ブラウザーがクラッシュします。
* ビューアを重複タップすると、ブラウザー側の拡大・縮小が有効になっているビューアだけでなく、ページ全体がズームされます。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* デバイスが、ブラウザー設定で「フルスクリーン」がチェックされた縦置きモードのタブレットとして検出されました。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアを重複タップすると、ビューアだけでなくページ全体がズームします。ブラウザ側の拡大・縮小が有効になっています。

## Galaxy Nexus 10およびGalaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalogで、見開きページが縦置きと横置きの方向に誤って表示される。

## HTCモバイルデバイス{#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできないのは、HTC UIラッパー(HTC Sense)の「機能」です。 この機能を使用すると、ビューアで「ピンチズーム」ジェスチャを使用した場合に、ページ全体がズームされる場合があります。 代わりに、重複タップジェスチャを使用します。
* 画像マップが小さく、近い場合に、画像マップのアイコンが重なります。

## HTML5ビデオビューア{#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修飾子は、ソフトウェアHLSとFlashHDSの再生でのみサポートされます。ネイティブプレーヤーを使用して再生している場合は機能しません。
* OGGおよびWebMのプログレッシブ再生はサポートされていません。
* ブラウザーの拡大/縮小により、ビデオプレーヤーが正しくないサイズで表示されます(Windows®Campaign コントロールパネル表示設定を含む)。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirksモードはサポートされていません。
* 互換モードがサポートされていません。
* モバイルのInternet Explorerはサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* iPad 2で大きなeCatalogを使用すると、ブラウザーがクラッシュする原因となります。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1以降：Flashのビデオを再生できないように、Internet Plug-inの設定を使用します。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない。
* HLSストリーミングを使用してSafari 6でビデオの最後までシークできません。
