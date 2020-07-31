---
title: コアコンポーネントの AMP サポート
description: コアコンポーネントは、AMP（Accelerated Mobile Pages）をサポートします
translation-type: ht
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: ht
source-wordcount: '493'
ht-degree: 100%

---


# コアコンポーネントの AMP サポート {#amp-support}

コアコンポーネントの[リリース 2.11.0](/help/versions.md) 以降で、[AMP（Accelerated Mobile Pages）](https://developers.google.com/amp)は完全にサポートされます。

このドキュメントでは、AMP のサポート方法の概要と、サイトで AMP を有効にする方法を説明します。ただし、技術的な詳細については、[GitHub 開発者ドキュメント](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)を参照してください。

## AMP とは {#what-is-amp}

Accelerated Mobile Pages（AMP）は、元々 Google がモバイルブラウジング用にページを最適化するために設計したオープンソースフレームワークです。通常、AMP ページは、標準の Web ページよりもさらに速く読み込まれ、優れたモバイルエクスペリエンスを提供します。

## コアコンポーネントの AMP {#amp-in-core-components}

コアコンポーネントでの AMP サポートは、[完全に設定可能です。](#enabling-amp)ページの AMP バージョンは、標準 HTML バージョンと一緒に排他的に提供する、またはまったく提供しないかを設定できます。

コアコンポーネントは、AMP ページをレンダリングするために Sling セレクターとして `amp` を使用します。例えば、`example.html` は通常のページをレンダリングし、`example.amp.html` は AMP バージョンになります。

### 要件 {#requirements}

AMP をコアコンポーネントと共に使用する場合、主な違いは、AMP では、最適化と共に、すべての CSS が `<head>` 要素内でインライン化される必要があるということです。

これをサポートするために、カスタマイズされたページコンポーネントが使用され、ページに存在するコンポーネントの AMP 固有の CSS のみが読み込まれます。

その他の要件および技術的な詳細については、[GitHub 開発者ドキュメント](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)を参照してください。

### コアコンポーネントでの AMP の使用 {#using-amp}

個々のプロジェクトで AMP を活用するかどうかを決定できます。さらに、AMP と標準の HTML ページは並行して提供できるので、プロジェクトの特定のページでのみ AMP を使用するように選択できます。

### AMP サポートのインストール {#installing-amp}

AMP はオプションなので、コアコンポーネントに拡張機能として提供されます。

* AEM as a Cloud Service プロジェクトの場合、拡張機能は自動的に使用可能になります。
* On-Premise および AMS プロジェクトの場合、コアコンポーネントのインストール時に、拡張機能を明示的にインストールする必要があります。

拡張機能がインストールされたら、コンポーネント作成者は、単に拡張機能内のスーパータイプを示すだけで済みます。

### ページに対する AMP の有効化 {#enabling-amp}

ページに対して AMP を有効にするには、[ページポリシー](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/authoring/siteandpage/templates.translate.html#editingatemplatepagepolicies)で **AMP モード**&#x200B;が選択されている必要があります。

![AMP ページポリシーのオプション](/help/assets/amp-policy.png)

* **AMP なし** - ページは標準の HTML としてのみ提供されます。
* **ペア AMP** - ページは、AMP および HTML として配信されます。
* **AMP のみ** - ページは AMP としてのみ提供されます。

ページの AMP 設定は、個々のページの[ページプロパティ](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/authoring/authoring/editing-page-properties.translate.html)で上書きすることもできます。

![AMP ページプロパティ](/help/assets/amp-page-properties.png)

* **ページテンプレートから継承** - これはデフォルト値で、ページテンプレートのポリシーから設定を取得できます。
* **AMP なし** - ページは標準の HTML としてのみ提供されます。
* **ペア AMP** - ページは、AMP および HTML として配信されます。
* **AMP のみ** - ページは AMP としてのみ提供されます。