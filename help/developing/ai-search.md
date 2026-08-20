---
title: コンテンツAI 検索コンポーネントの設定
description: コンテンツAI 検索コンポーネントは、生成AIを利用した検索でサイト訪問者に提供します。 コンテンツ作成者に対してこのコンポーネントを有効にする方法について説明します。
role: Developer, Admin
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
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# コンテンツAI 検索コンポーネントの設定 {#configure-content-ai-search-component}

コンテンツAI 検索コンポーネントは、生成AIを利用した検索でサイト訪問者に提供します。 コンテンツ作成者に対してこのコンポーネントを有効にする方法について説明します。

## 前提条件 {#prerequisites}

* 少なくとも1つの[Content Source](https://experienceleague.adobe.com/ja/docs/experience-manager-content-ai/using/contentsources)が既に作成され、ステータスは&#x200B;**Available**&#x200B;です。
* 有効なAPI資格情報と&#x200B;**デフォルトのContent Source**&#x200B;値を使用して、オーサーとパブリッシュの両方で設定された&#x200B;**AEM Content AI Client** OSGi設定（`ContentAIClientImpl`）。 資格情報の取得方法については、[Adobe Developer Console プロジェクトの設定](https://experienceleague.adobe.com/ja/docs/experience-manager-content-ai/using/setup-adc-project)のドキュメントを参照してください。

## プロキシコンポーネントの作成 {#proxy-component}

すべてのコアコンポーネントと同様に、AEMに付属するデフォルトのコンテンツAI 検索コンポーネントのプロキシコンポーネントを作成することをお勧めします。 プロキシコンポーネントのプロジェクト固有の変更を`/apps`の下に置くと、`/libs`の下のベースコンポーネントがAdobeによって自動的に更新され、プロジェクトコンポーネントはこれらの更新を自動的に継承します。 詳しくは、[&#x200B; コアコンポーネントの使用](/help/get-started/using.md#aemaacs)および[&#x200B; コンポーネントガイドライン &#x200B;](/help/developing/guidelines.md)のドキュメントを参照してください。

## クライアントライブラリの設定 {#clientlib}

コンテンツAI 検索コンポーネントは、コアコンポーネントにクライアントライブラリを含めるための標準パターン [に従っていません。](/help/developing/including-clientlibs.md) 代わりに、次の手順に従います。

プロジェクトのページコンポーネント `customheaderlibs.html` （CSS）および`customfooterlibs.html` （JS）に次を追加します。

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

プロジェクトに独自のブランドスタイルが適用されている場合は、プロジェクトのクライアントライブラリの2番目のカテゴリをこのカテゴリの後に追加します。

## コンテンツAI 検索コンポーネントの使用 {#using}

コンテンツ作成者は、コンテンツAI 検索コンポーネントをページに配置できるようになりました。 詳しくは、[&#x200B; コンテンツAI 検索コンポーネント &#x200B;](/help/components/ai-search.md)のドキュメントを参照してください。

## コンポーネントでコンテンツ AIを使用する方法 {#how-it-works}

* 標準的な検索クエリは、Content Sourceのインデックスと同じ取得レイヤーによって提供され、設定されたソースから一致するページ、フラグメント、またはアセットを返します。
* AI生成の概要が有効になっている場合、コンポーネントはAEM Content AI生成エンドポイントを追加的に呼び出し、同じインデックス付きコンテンツで応答をグラウンディングし、サマリーにソースを表示して訪問者が検証できるようにします。
* 両方の機能は同じ管理されたContent Sourceから読み取られるため、結果と概要は、現在インデックスに登録されているコンテンツと一貫性を維持します。 取得を再実行すると（[&#x200B; コンテンツソースの制御](https://experienceleague.adobe.com/ja/docs/experience-manager-content-ai/using/contentsources)を参照）、両方が更新されます。

## 次の手順 {#next-steps}

* [&#x200B; コンテンツソースを管理](https://experienceleague.adobe.com/ja/docs/experience-manager-content-ai/using/contentsources) – このコンポーネントが検索するコンテンツSourceを作成および管理します。
* [Adobe Developer Console プロジェクトの設定](https://experienceleague.adobe.com/ja/docs/experience-manager-content-ai/using/setup-adc-project) — OSGi Content AI クライアント設定で使用される資格情報を取得します。
* [&#x200B; コンテンツ AI API リファレンス &#x200B;](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) – このコンポーネントが呼び出す基礎となる検索と生成サマリーエンドポイントを理解します。
