---
title: テンプレート
description: テンプレートを使用して、複数の画像レイヤーを合成するリクエストや、rtf形式のテキストを含むリクエストの長さと複雑さを軽減できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
TQID: 'https://experienceleague.adobe.com/FFRoxO7iVDzE7Kta5Vig4RtaPWa890tNHPwsAOcWVCw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 0%

---

# テンプレート{#templates}

テンプレートを使用して、複数の画像レイヤーを合成するリクエストや、rtf形式のテキストを含むリクエストの長さと複雑さを軽減できます。

カスタム変数を使用すると、テンプレートの使用をさらに簡素化できます。 多くの場合、テンプレートは、画像やテキストの入れ替えや、実行時にその他のオプションを簡単に設定できるように設定されます。

テンプレートは画像カタログにレコードとして保存され、テンプレート本文は`catalog::Modifier` フィールドに格納され、`catalog::Path` フィールドは空であるか、動的に変更できない静的背景画像を指定します。

テンプレートは、`template=` コマンドまたはリクエスト URLのパスコンポーネントで指定します。 ほとんどのアプリケーションでは、`template=` コマンドを使用してテンプレートを指定することをお勧めします。 `template=` コマンドは`catalog::PostModifier` フィールドで実行してはならず、ネストされたIS リクエストの`catalog::Modifier` フィールド （つまり、`src=is{...}` コンストラクト）でのみ実行できます。 テンプレートレコードは、`src=`または`mask=` コマンドで参照できません。

テンプレートに埋め込まれた`src=`または`mask=` コマンドは、リクエストのメインカタログまたは別の画像カタログに解決できます。 `rootId`が明示的に指定されていない場合、メインカタログが想定されます。 `template=`で指定されたテンプレートは、メインカタログまたは別の画像カタログに配置することもできます。

テンプレートで使用されるすべての変数のデフォルト定義を常に含めることを強くお勧めします。 この方法では、テンプレートで使用されている変数を知らなくても、`attribute::RootId`と`catalog::Id`を指定するだけで、テンプレートの画像出力を常に表示できます。

定義済みのパス置換変数`$object$`を使用して、URL パスで指定された画像オブジェクトを、ネストされたリクエストまたは埋め込まれたリクエストでも、任意のレイヤーソースまたはマスク（`src=`または`mask=`）に適用できます。

* [例A](r-example-a.md)
* [例B](r-example-b.md)
* [例C](r-example-c.md)
