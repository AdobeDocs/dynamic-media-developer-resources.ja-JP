---
title: 周辺光量変換
description: Vignette Converter （vntc）は、画像レンダリングを使用してデプロイメント用に画像オーサリングで作成されたコンテンツを準備するために使用されるコマンドラインユーティリティです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# 周辺光量変換{#vignette-converter}

Vignette Converter （vntc）は、画像レンダリングを使用してデプロイメント用に画像オーサリングで作成されたコンテンツを準備するために使用されるコマンドラインユーティリティです。

[!DNL vntc]は[!DNL *[!DNL install_root]*\ImageServing\bin]にあります。 次の機能があります。

* プライマリビネットを単解像度、多解像度、またはピラミッドの実稼動ビネットに変換します（[&#x200B; ビネットの拡大・縮小](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)を参照）。
* 実稼動キャビネットとウィンドウのカバーするスタイルファイルを作成します（`-resolution`および`-jpegquality`を参照）。

* ビネット、キャビネット、およびウィンドウ カバリングの様々なファイル バージョンを作成して、古いバージョンの画像レンダリングで使用するスタイル ファイルを作成します。
* 全解像度またはサムネールを含むビネットからビュー画像を抽出します（`-thumbwidth`および`-image`を参照）。
* ソースファイル（`-info`を参照）から関連プロパティを抽出し、それらを`stdout`またはオプションのログファイル（`-log`を参照）に送信します。

[!DNL vntc]の使用はオプションですが、Adobeでは最適なサーバーパフォーマンスを実現するためにこの使用をお勧めします。 また、Vignette Converterは大規模なエラーチェックを実装し、真剣に使用すると、クラッシュなどの深刻なサーバー問題を防ぐことができます。

実稼動ビネットを生成する場合、出力ビネットのピクセル幅（ピラミッドまたは多解像度ビネットの場合は0）が、生成された出力ビネットファイルの名前に追加されます。 キャビネットスタイルファイルを処理する場合、出力ファイル名に出力解像度が追加されます。 オプションのサムネール、画像、ログファイルおよび実稼動ビネットまたはキャビネットスタイルファイルを含むすべての出力ファイルは、*[!DNL sourceFile]*&#x200B;が配置されているディレクトリと同じディレクトリに配置されます（`-destPath`が指定されていない場合）。

Vignette Converterは、デフォルトでは最大3 GBのメモリに制限されています。 vntcがこの制限に達すると、処理が停止し、エラーが発生します。 この制限は、`-maxmem`を使用して変更できます。

>[!NOTE]
>
>画像オーサリングの周辺光量補正ツールを使用して、画像レンダリング用の周辺光量補正を準備することもできます。 同様に、コンテンツオーサリングツールは、画像レンダリングで使用するキャビネットスタイルファイルを生成できます。 処理を自動化する場合は、[!DNL vntc]を使用してください。 画像オーサリングのツールにはグラフィカルユーザーインターフェイスが含まれているため、通常はインタラクティブに使用しやすくなります。

## 関連項目 {#section-3c756bf17b634543904fdd928adeafb2}

画像オーサリングドキュメント

