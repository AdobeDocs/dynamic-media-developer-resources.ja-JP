---
title: 互換性に関する注意
description: オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関するメモ。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# 互換性に関する注意{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザーおよびモバイルデバイスの互換性に関するメモ。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとの非互換性。 再生を許可するには、アダプティブビデオセットを再アップロードします。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側での拡大/縮小により、ユーザーがページにズームインすると、UI と画像がぼやけてしまいます。 また、ユーザーインターフェイスの書式設定も、ズームに応じて正しく表示されず、全画面表示に引き継がれます。
* モバイルデバイスのサイズ制限により、混在メディアビューアでは、埋め込みスウォッチコンポーネントをタップする代わりに、スライドジェスチャを使用して埋め込み画像セット内のフレームを入れ替えます。 コンポーネントは、視覚的なインジケーターとして表示されます。
* Internet Explorer ブラウザーおよび一部のタッチデバイスでは、フルスクリーンモードでデバイス画面全体が占有されません。 代わりに、アプリケーションのサイズをブラウザーウィンドウのサイズに変更します。
* 閉じるボタンは、iOS 8.0 およびiOS 8.1 では機能しませんが、iOS 8.2 では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Zoom ビューアと eCatalog ビューアでメモリリークが見られる。 フレーム間を繰り返し移動すると、ブラウザーがクラッシュする。
* ビューアをダブルタップすると、ブラウザー側の拡大/縮小が有効になっているビューアだけでなく、ページ全体がズームされます。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* デバイスが縦置きモードでタブレットとして検出され、ブラウザー設定で「フルスクリーン」がオンになっている。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアをダブルタップすると、ブラウザー側の拡大/縮小が有効になって、ビューアだけでなくページ全体がズームされます。

## Galaxy Nexus 10 と Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog で、縦長および横長の向きの間に見開きのページが正しく表示されない問題を修正しました。

## HTC モバイルデバイス {#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできないことは、HTC UI ラッパー (HTC Sense) の「機能」です。 この機能を使用すると、ビューアで「ピンチツーズーム」ジェスチャを使用した場合に、ページ全体がズームする可能性があります。 代わりにダブルタップジェスチャを使用してください。
* 画像マップが小さく、互いに近い場合に、画像マップアイコンが重なります。

## HTML5 ビデオビューア {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修飾子は、ソフトウェア HLS とFlashHDS の再生でのみサポートされます。 再生がネイティブプレーヤーを使用している場合は機能しません。
* OGG および WebM のプログレッシブ再生はサポートされていません。
* ブラウザーの拡大/縮小により、ビデオプレーヤーのサイズが正しく表示されません (Windows®のCampaign コントロールパネル表示設定を含む )。
* Safari での HLS ストリーミングを使用したビデオのシークに一貫性がありません。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks モードはサポートされていません。
* 互換性モードはサポートされていません。
* モバイル版の Internet Explorer はサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* eCatalog が大きいと、iPad 2 でブラウザがクラッシュする。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 以降：インターネットプラグインの設定により、Flashビデオを再生できません。
* Safari での HLS ストリーミングを使用したビデオのシークに一貫性がありません。
* HLS ストリーミングを使用して Safari 6 でビデオの終わりをシークできません。
