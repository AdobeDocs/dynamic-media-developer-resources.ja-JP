---
description: オペレーティングシステム、ブラウザー、モバイルデバイスの互換性に関する注意事項。
solution: Experience Manager
title: 互換性に関する注意
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# 互換性に関する注意{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザー、モバイルデバイスの互換性に関する注意事項。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとの非互換性。 再生を許可するには、アダプティブビデオセットを再アップロードします。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側の拡大/縮小により、ユーザーがページにズームインすると、UIと画像がぼやけます。 また、ズームに応じて、ユーザーインターフェイスの形式設定が正しく表示されず、全画面表示に引き継がれます。
* モバイルデバイスのサイズ制限により、混在メディアビューアでは、埋め込みスウォッチコンポーネントをタップする代わりに、スライドジェスチャを使用して埋め込み画像セット内のフレームを入れ替えます。 コンポーネントは、視覚的なインジケーターとして表示されます。
* Internet Explorerブラウザーや一部のタッチデバイスでは、フルスクリーンモードではデバイス画面全体が占有されません。 代わりに、アプリケーションのサイズがブラウザーウィンドウのサイズに変更されます。
* 閉じるボタンはiOS 8.0およびiOS 8.1では機能しませんが、iOS 8.2では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* ズームビューアおよびeCatalogビューアでメモリリークが見られる。 フレーム間を繰り返し移動すると、ブラウザーがクラッシュする。
* ビューアをダブルタップすると、ブラウザー側の拡大縮小が有効になっているビューアだけでなく、ページ全体がズームされます。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* デバイスが縦置きモードでタブレットとして検出され、ブラウザー設定で「フルスクリーン」がオンになっている。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアをダブルタップすると、ブラウザー側の拡大・縮小が有効になっている状態で、ビューアだけでなくページ全体がズームします。

## Galaxy Nexus 10とGalaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalogで、縦長および横長の向きの間違ったページ見開きが表示される。

## HTCモバイルデバイス {#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできないのは、HTC UIラッパー(HTC Sense)の「機能」です。 この機能を使用すると、ビューアで「ピンチズーム」ジェスチャを使用した場合に、ページ全体がズームする可能性があります。 代わりに、ダブルタップジェスチャを使用してください。
* 画像マップが小さく、互いに近い場合に画像マップアイコンが重なります。

## HTML5ビデオビューア {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修飾子は、ソフトウェアHLSとFlashHDSの再生でのみサポートされます。再生でネイティブプレーヤーが使用されている場合は機能しません。
* OGGおよびWebMのプログレッシブ再生はサポートされていません。
* ブラウザーの拡大/縮小により、ビデオプレーヤーのサイズが正しく表示されない(Windows®のCampaign コントロールパネル表示設定を含む)。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirksモードはサポートされていません。
* 互換モードはサポートされていません。
* モバイル上のInternet Explorerはサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* iPad 2で大きなeCatalogを使用すると、ブラウザがクラッシュする。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1以降：インターネットプラグインの設定により、Flashビデオを再生できません。
* SafariでのHLSストリーミングを使用したビデオシークに一貫性がない。
* HLSストリーミングを使用してSafari 6でビデオの最後までシークできない。
