---
description: オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関する注意事項。
seo-description: オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関する注意事項。
seo-title: 互換性に関する注意
solution: Experience Manager
title: 互換性に関する注意
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# 互換性に関する注意{#compatibility-notes}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関する注意事項。

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとは互換性がありません。 アダプティブビデオセットを再アップロードして再生する必要が生じる場合があります。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側での拡大縮小により、ユーザーがページにズームインすると、UIや画像がぼやける場合があります。 ズームによっては、UIの形式設定も正しく表示されない場合があります。 これはフルスクリーンに引き継がれます。
* モバイルデバイスのサイズ制限により、混在メディアビューアでは、埋め込みのスウォッチコンポーネントをタップする代わりに、スライドジェスチャを使用して埋め込み画像セット内のフレームを入れ替えます。 コンポーネントは視覚的なインジケーターとして存在します。
* Internet Explorerブラウザーおよび一部のタッチデバイスでは、フルスクリーンモードではデバイス画面全体が表示されません。 代わりに、ブラウザーウィンドウのサイズに合わせてアプリケーションのサイズが変更されます。
* 閉じるボタンはiOS 8.0およびiOS 8.1では機能しませんが、iOS 8.2では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* ズームビューアおよびeCatalogビューアでメモリリークが見られます。 フレーム間を繰り返しナビゲーションすると、ブラウザーがクラッシュする場合があります。
* ビューアを重複タップすると、ブラウザー側の拡大・縮小が有効になっているビューアだけでなく、ページ全体がズームされる場合があります。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* デバイスが、ブラウザー設定で「フルスクリーン」がチェックされた縦置きモードのタブレットとして検出されました。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアを重複タップすると、ブラウザー側の拡大・縮小が有効な場合に、ビューアだけでなくページ全体がズームされる場合があります。

## Galaxy Nexus 10およびGalaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalogで、見開きページが縦置きと横置きの方向に誤って表示される。

## HTCモバイルデバイス {#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできないのは、HTC UIラッパー(HTC Sense)の「機能」です。 この機能を使用すると、ビューアで「ピンチズーム」ジェスチャを使用した場合に、ページ全体がズームされる場合があります。 代わりに、重複タップジェスチャを使用します。
* 画像マップが小さく、近い場合に、画像マップのアイコンが重なる場合があります。

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifierは、ソフトウェアHLSおよびFlash HDSの再生でのみサポートされます。 ネイティブプレーヤーを使用して再生している場合は機能しません。
* OGGおよびWebMのプログレッシブ再生はサポートされていません。
* ブラウザーを拡大縮小すると、ビデオプレーヤーが正しくないサイズで表示される場合があります（Windows OSコントロールパネルの「ディスプレイ」設定が含まれます）。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない場合があります。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirksモードはサポートされていません。
* 互換モードがサポートされていません。
* モバイルのInternet Explorerはサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* iPad 2で大きなeCatalogを作成すると、ブラウザーがクラッシュする場合があります。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1以降： Internet Plug-inの設定により、Flashビデオを再生できない場合があります。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない場合があります。
* HLSストリーミングを使用してSafari 6でビデオの最後までシークできません。

