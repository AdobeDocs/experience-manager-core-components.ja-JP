---
title: コアコンポーネントの AMP サポート
description: コアコンポーネントは、AMP（Accelerated Mobile Pages）をサポートします
role: Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
TQID: https://experienceleague.adobe.com/5v1tXLzHNRvAxy6-aJipN-ZYzsPJ1xFNc1hKmz73wic
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 59ca85e0f0b99ba46bb2b85f383f1fefd2b1c5fd
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 76%

---


# コアコンポーネントの AMP サポート {#amp-support}

コアコンポーネントの[リリース 2.11.0](/help/versions.md) 以降で、[AMP（Accelerated Mobile Pages）](https://developers.google.com/amp)は完全にサポートされます。

このドキュメントでは、AMP のサポート方法の概要と、サイトで AMP を有効にする方法を説明します。 ただし、技術的な詳細については、[GitHub 開発者ドキュメント](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)を参照してください。

## AMP とは {#what-is-amp}

Accelerated Mobile Pages（AMP）は、元々 Google がモバイルブラウジング用にページを最適化するために設計したオープンソースフレームワークです。 通常、AMP ページは、標準の Web ページよりもさらに速く読み込まれ、優れたモバイルエクスペリエンスを提供します。

## コアコンポーネントの AMP {#amp-in-core-components}

コアコンポーネントでの AMP サポートは、[完全に設定可能です。](#enabling-amp) ページの AMP バージョンは、標準 HTML バージョンと一緒に排他的に提供する、またはまったく提供しないかを設定できます。

コアコンポーネントは、AMP ページをレンダリングするために Sling セレクターとして `amp` を使用します。 例えば、`example.html` は通常のページをレンダリングし、`example.amp.html` は AMP バージョンになります。

個々のプロジェクトで AMP を活用するかどうかを決定できます。 さらに、AMP と標準の HTML ページは並行して提供できるので、プロジェクトの特定のページでのみ AMP を使用するように選択できます。

## プロジェクトでの AMP サポートの使用の手引き {#getting-started}

AMP サポートは高い柔軟性を提供しますが、これを使い始めるには、いくつかの簡単な手順が必要です。

1. [コアコンポーネントのインストール](/help/get-started/using.md#download-and-install)
   * AEM as a Cloud Service プロジェクトの場合、コアコンポーネントはデフォルトで使用でき、追加のインストールは必要ありません。
   * オンプレミスおよびAMS プロジェクトの場合は、[GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest)からコアコンポーネントの最新のコンテンツパッケージをダウンロードし、AEM環境にインストールできます。
   * オンプレミスまたはAMS プロジェクトで2.14.0より前のコアコンポーネントリリースを使用している場合は、GitHubのリリースの一部として利用可能なAMP拡張機能もインストールする必要があります。
1. コンポーネント `resourceSuperType`を`core/wcm/extensions/amp/components/page/v1/page`にポイントします。
   * お勧めのベストプラクティスとして[AEM プロジェクトアーキタイプ &#x200B;](/help/developing/archetype/using.md)を使用し、AMP サポートを有効にする[&#x200B; オプションを選択した場合、](https://github.com/adobe/aem-project-archetype/tree/develop)これは自動的に実行されました。
1. テンプレートレベルまたは個々のページで、[AMP サポートを有効にします](#enabling-amp)。
1. 必要に応じて、インライン [CSS をデプロイします](#css-requirements)。

### ページに対する AMP の有効化 {#enabling-amp}

ページに対して AMP を有効にするには、[ページポリシー](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja#editing-a-template-page-policy-template-author-developer)で **AMP モード**&#x200B;が選択されている必要があります。

![AMP ページポリシーのオプション](/help/assets/amp-policy.png)

* **AMP なし** - ページは標準の HTML としてのみ提供されます。
* **ペア AMP** - ページは、AMP および HTML として配信されます。
* **AMP のみ** - ページは AMP としてのみ提供されます。

ページの AMP 設定は、個々のページの[ページプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=ja)で上書きすることもできます。

![AMP ページプロパティ](/help/assets/amp-page-properties.png)

* **ページテンプレートから継承** - これはデフォルト値で、ページテンプレートのポリシーから設定を取得できます。
* **AMP なし** - ページは標準の HTML としてのみ提供されます。
* **ペア AMP** - ページは、AMP および HTML として配信されます。
* **AMP のみ** - ページは AMP としてのみ提供されます。

これらのオプションは、`resourceSuperType`がAMP サポート用に正しく設定されている場合にのみUIに表示されます。 デフォルトのWKND サンプルコンテンツには`resourceSuperType`が設定されていないため、AMPのオプションはUIに表示されません。

### CSS の要件 {#css-requirements}

AMP をコアコンポーネントと共に使用する場合、主な違いは、AMP では、`<head>` 要素内で[すべての CSS をインライン化](including-clientlibs.md#inlining)および最適化する必要があるということです。

これをサポートするために、カスタマイズされたページコンポーネントが使用され、ページに存在するコンポーネントの AMP 固有の CSS のみが読み込まれます。

>[!NOTE]
>
>AMP デザインの制約により、アドビは、ページの AMP バージョンでレスポンシブグリッドを使用することをサポートしません。

その他の要件および技術的な詳細については、[GitHub 開発者ドキュメント](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)を参照してください。
