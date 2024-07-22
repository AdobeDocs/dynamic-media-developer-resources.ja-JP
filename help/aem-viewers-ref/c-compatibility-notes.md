---
title: 互換性に関する注意事項
description: オペレーティングシステム、ブラウザー、モバイルデバイス向けの互換性に関するメモ。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# 互換性に関する注意事項{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

オペレーティングシステム、ブラウザー、モバイルデバイス向けの互換性に関するメモ。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 古いアダプティブビデオセットとの非互換性。 アダプティブビデオセットを再度アップロードして、再生できるようにします。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* ブラウザー側の拡大縮小により、ユーザーがページにズームすると UI と画像がぼやけます。 ズームに応じて、ユーザーインターフェイスの書式設定が正しく表示されず、全画面に引き継がれます。
* モバイルデバイスでのサイズ制限により、混在メディアビューアでは、埋め込みスウォッチコンポーネントをタップする代わりに、スライドジェスチャーを使用して埋め込み画像セット内のフレームを入れ替えます。 コンポーネントは、視覚的なインジケーターとして存在します。
* Internet Explorer のブラウザーや一部のタッチデバイスでは、フルスクリーンモードがデバイスの画面全体を占めることはありません。 代わりに、アプリケーションのサイズがブラウザーウィンドウのサイズに変更されます。
* 「閉じる」ボタンは、iOS 8.0 およびiOS 8.1 では機能しませんが、iOS 8.2 では機能します。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* ズームビューアと eCatalog ビューアでメモリリークが発生する。 フレーム間でナビゲーションを繰り返すと、ブラウザがクラッシュする。
* ビューアをダブルタップすると、ブラウザー側の拡大縮小を有効にしたビューアだけでなく、ページ全体がズームされます。

## ギャラクシー S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* ブラウザー設定でフルスクリーンがオンの状態で、デバイスが縦向きモードでタブレットとして検出されました。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* ビューアをダブルタップすると、ブラウザー側の拡大縮小を有効にした状態で、ビューアだけでなく、ページ全体がズームされます。

## Galaxy Nexus 10 と Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog で、縦向きと横向きの見開きが正しく表示されない。

## HTC モバイルデバイス {#section-dc42c80414c842e488738fc157c55b01}

* ネイティブのピンチズームを無効にできないのは、HTC UI ラッパー（HTC Sense）の「機能」です。 この機能により、ビューアで「ピンチでズーム」ジェスチャーを使用した場合に、ページ全体がズームされることがあります。 代わりに、ダブルタップのジェスチャーを使用します。
* 画像マップが小さく、接近している場合、画像マップのアイコンが重なります。

## HTML5 ビデオビューア {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修飾子は、ソフトウェア HLS およびFlash HDS 再生でのみサポートされます。 再生がネイティブプレーヤーを使用している場合は機能しません。
* OGG および WebM プログレッシブ再生はサポートされていません。
* ブラウザーの拡大縮小により、ビデオプレーヤーのサイズが正しく表示されません（Windows® Campaign コントロールパネルーのディスプレイ設定を含む）。
* Safari での HLS ストリーミングを使用したビデオシークに一貫性がない。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 互換モードはサポートされていません。
* 互換モードはサポートされていません。
* モバイルの Internet Explorer はサポートされていません。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大きな eCatalog があると、iPad 2 でブラウザーがクラッシュします。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 以降：インターネットプラグインの設定により、Flashビデオは再生できません。
* Safari での HLS ストリーミングを使用したビデオシークに一貫性がない。
* HLS ストリーミングを使用する Safari 6 でビデオの終わりをシークできない。
