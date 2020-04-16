---
title: コアコンポーネントを使用した成功へのパス
description: コアコンポーネントを使用したプロジェクトの実装を成功させる方法
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# コアコンポーネントを使用した成功へのパス {#paths-to-success}

コアコンポーネントは、強力で柔軟性が高く、使いやすく、カスタマイズも簡単です。 このドキュメントで概要を説明するいくつかの主要なガイドラインに従うと、コアコンポーネントを含むプロジェクトが確実に成功します。

## 成功への2つのパス {#two-paths}

コアコンポーネントの実装には2つの基本的なアプローチがあり、成功につながりますが、プロジェクトごとに考慮する必要のある独自のトレードオフを持っています。

1. デザインをコアコンポーネントにマップし、提供されるHTMLを取り込みます。 または
1. 定義済みのHTML標準に準拠する必要がある場合は、コアコンポーネントの利点をすべて活用する必要はなく、より多くの労力が必要になります。

## コンポーネントの実装に共通する問題 {#common-pitfalls}

コアコンポーネントでプロジェクトが成功しない原因となる2つの一般的な問題は、次のとおりです。

* **最終設計** - Cレベルの承認を得て、基盤となる技術に関係なくピクセルパーフェクトな実装を行うために開発チームに引き継がれる場合もあります。
* **会社規模のHTMLスタイルガイド** — このようなガイドは、トップダウンの観点からスタイルを適用するコンポーネントによって決められて実行されることが多くあります。

どちらの場合も、コンポーネントに対する要件が非常に厳しく、特定の要件を満たすので、コアコンポーネントやそのまま使用できるコンポーネントを遵守するのは困難で、カスタムコンポーネントの大規模な開発につながります。

## 開始早期 {#start-early}

プロジェクトの導入段階でコアコンポーネントを考慮するだけでなく、ワイヤフレームおよび設計段階でコアコンポーネントとの開始を既に検討しています。

### コンポーネントライブラリの使用 {#component-library}

既に設計段階に [あるコンポーネント](https://adobe.com/go/aem_cmp_library_jp) ・ライブラリを参照します。 コアコンポーネントは強力で柔軟性が高く、出発点としての役割を果たします。 コアコンポーネントを使用して実際に合理的に達成できない真のビジネスニーズがある場合にのみ、カスタムコンポーネントを追加します。

### Adobe XD用UIキットの使用 {#ui-kit}

カスタムコンポーネントのニーズが明らかになったら、 [UIキットをAdobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) （UIキット）を活用して、デザイナーがワイヤフレームの構築と、コアコンポーネントを構築ブロックとして使用したデザインの構築を開始できるようにします。

## 強力な機能を見過ごすな {#powerful-features}

AEMとコアコンポーネントの機能は非常に強力ですが、非常に微妙で、特定の機能の可能性がデザイナーにはすぐには明らかにならない場合があります。

### コンテンツフラグメント {#content-fragments}

[コンテンツフラグメントを使用すると、チャネルに特化しないコンテンツをチャネル固有のバリエーションと共に作成できます。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html)その後、コンテンツページをオーサリングする際に、これらのフラグメントとそれらのバリエーションを使用できます。

更新された JSON エクスポーターと共に構造化コンテンツフラグメントを使用して、AEM コンテンツをコンテンツサービス経由で AEM ページ以外のチャネルに配信することもできます。

### エクスペリエンスフラグメントテンプレート {#experience-fragment-templates}

作成者がページの一部（エクスペリエンスのフラグメント）を再利用する場合。
Without [Experience Fragments,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) the author would need to copy and paste that fragment. これらのエクスペリエンスのコピー／貼り付けの作成と管理には時間がかかり、ユーザーエラーが発生しがちです。
エクスペリエンスフラグメントは、コピー／貼り付けを不要にします。

### 埋め込みコンポーネント {#embed-component}

[埋め込みコンポーネントは](/help/components/embed.md) 、YouTubeビデオコンテンツなどの外部リソースを単に含めるだけでなく、プロジェクトのニーズに合わせてコンテンツを収容できるように拡張可能です。