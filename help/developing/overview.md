---
title: コアコンポーネントの開発
description: コアコンポーネントは、豊富な機能、継続的配信、コンポーネントのバージョン管理、最新の実装、効率的なマークアップ、コンテンツの JSON エクスポートなどの特長を持つ堅牢で拡張可能なベースコンポーネントを提供します。
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: ht
source-wordcount: '1130'
ht-degree: 100%

---

# コアコンポーネントの開発 {#developing-core-components}

コアコンポーネントは、豊富な機能、継続的配信、コンポーネントのバージョン管理、最新の実装、効率的なマークアップ、コンテンツの JSON エクスポートなどの特長を持つ堅牢で拡張可能なベースコンポーネントを提供します。

{{traditional-aem}}

## コアコンポーネントの利用でプロジェクトを成功に導く方法 {#how-to-succeed}

コアコンポーネントは、強力で柔軟性が高く、使いやすく、カスタマイズも簡単です。[いくつかの主要なガイドラインに従えば](success.md)、コアコンポーネントを利用したプロジェクトを確実に成功させることができます。

## コアコンポーネントへの移行

新規プロジェクトは、コアコンポーネントで実装する必要があります。ただし、既存プロジェクトでは通常、基盤コンポーネントが広範囲にわたって実装されています。

### 基盤コンポーネントからの移行 {#from-foundation}

既存プロジェクトに関する大規模な作業（リブランディングや全体的なリファクタリングなど）は、多くの場合、コアコンポーネントへの移行のチャンスとなります。このような移行を容易にするために、アドビでは、コアコンポーネントと最新の AEM テクノロジーの導入を促進するための多数の移行ツールを提供しています。

[AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/) を使用すると、以下の変換を容易に行えるようになります。

* 静的テンプレートから編集可能テンプレートへ
* デザイン設定からポリシーへ
* 基盤コンポーネントからコアコンポーネントへ
* クラシック UI からタッチ操作対応 UI へ

これらのツールの使用方法について詳しくは、[ぞれぞれのドキュメント](https://opensource.adobe.com/aem-modernize-tools/)を参照してください。

>[!NOTE]
>
>AEM Modernize Tools はコミュニティの取り組みであり、アドビによるサポートまたは保証の対象外です。

## AEM as a Cloud Service への移行を通じた移行 {#via-aemaacs}

AEM as a Cloud Service には最新版のコアコンポーネントが自動的に搭載されているので、オンプレミスの AEM から移行する場合は、プロジェクトの `pom.xml` ファイルでコアコンポーネントへの依存関係を削除する必要があります。

プロキシは必要なスーパータイプを指しており、そのスーパータイプのパスにバージョンが含まれているので、プロキシコンポーネントは引き続きこれまでどおり機能します。このようにして、依存関係を削除するだけで、コアコンポーネントはオンプレミスの場合と同じように AEM as a Cloud Service で動作させることができます。

他の AEM as a Cloud Service プロジェクトと同様に、AEM SDK JAR への依存関係も追加する必要があります。これはコアコンポーネントに限ったことではありませんが、いずれにせよ必要なことです。

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

AEM as a Cloud Service プロジェクトについて詳しくは、[AEM プロジェクトの構造](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=ja)を参照してください。

## コアコンポーネントのサポート {#core-component-support}

コアコンポーネントは AEM に不可欠な部分なので、クイックスタートの一部として提供される場合と同じ条件の下、現状のままでサポートされます。

他の AEM 製品機能と同様、原則的としてまず、コンポーネントの廃止が発表されてから、最短でその次のリリースで削除されます。これにより、サポートが終了する前に、コンポーネントの新バージョンに移行する猶予期間として少なくとも 1 回分のリリースサイクルを確保できます。

各コンポーネントのバージョンには、サポートされる AEM バージョンが明記されています。ある AEM バージョンのサポートが停止されると、その AEM バージョンでのコアコンポーネントのサポートも停止されます。

コンポーネントのカスタマイズのサポートについて詳しくは、[コアコンポーネントのカスタマイズ](customizing.md)を参照してください。


## 技術的機能 {#technical-capabilities}

コアコンポーネントと基盤コンポーネントの違いを次の表に大まかに示します。

オーサリング機能とそれらの機能を事前に設定するためのオプションについて詳しくは、[コアコンポーネントを使用したオーサリング](/help/get-started/authoring.md)を参照してください。

| **機能** | **コアコンポーネント** | **基盤コンポーネント** |
|-----|---|---|
| ロジックの実装 | [Sling モデル](https://sling.apache.org/documentation/bundles/models.html)注釈の付いた Java POJO | JSP コード |
| マークアップ定義 | [HTML テンプレート言語](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=ja)（HTL）構文 | JSP コード |
| XSS サニタイズ | HTL で自動化 | ほぼ手動 |
| CSS クラスの命名 | [ブロック要素修飾子](https://getbem.com/)（BEM）表記（リリース 2.0.0 時点）に基づく、標準化された命名規則 | カスタムスキーム |
| ダイアログの定義 | [Coral 3](https://helpx.adobe.com/jp/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + クラシック UI |
| JSON 出力 | [Jackson シリアル化を使用している Sling モデルエクスポーター](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | デフォルト Sling サーブレット |
| バージョン管理 | [モデルと HTL の場合](guidelines.md) | なし |
| テスト | 単体テスト + 統合テスト | 統合テスト |
| 配信 | [公開 GitHub 経由](https://github.com/adobe/aem-core-wcm-components) | クイックスタートを通じて |
| ライセンス | [Apache ライセンス](https://www.apache.org/licenses/LICENSE-2.0) | アドビ固有 |
| 貢献度 | プル要求を通じて | 不可能 |
| アクセシビリティ | [WCAG 2.0 AA 標準](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=ja)に完全に準拠 | [WCAG 2.0 AA 標準](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=ja)に部分的に準拠 |

## コンポーネントリスト {#component-list}

使用可能なコアコンポーネント（API へのリンク）と、コアコンポーネントに置き換わる基盤コンポーネントの一覧を次の表に示します。

| コアコンポーネント | 説明 | 置き換わる基盤コンポーネント |
|---|---|---|
| [ページ](https://adobe.com/go/aem_cmp_tech_page_v2_jp) | テンプレートエディターに対応するレスポンシブページ | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [パンくず](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_jp) | ページ階層のナビゲーション | `/libs/foundation/components/breadcrumb` |
| [タイトル](https://adobe.com/go/aem_cmp_tech_title_v2_jp) | H1 ~ H6 タイトル | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [テキスト](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | リッチテキスト | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [画像](https://adobe.com/go/aem_cmp_tech_image_v2_jp) | 最適なレンディションサイズのスマート遅延読み込み | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [リスト](https://adobe.com/go/aem_cmp_tech_list_v2_jp) | ページのリスト | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [ソーシャルメディア共有](https://adobe.com/go/aem_cmp_tech_sharing_v1_jp) | Facebook および Pinterest の共有ウィジェット | `-` |
| [フォームコンテナ](https://adobe.com/go/aem_cmp_tech_form_container_v2_jp) | レスポンシブフォームの段落システム | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [フォームテキスト](https://adobe.com/go/aem_cmp_tech_form_text_v2_jp) | テキスト入力フィールド | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [フォームオプション](https://adobe.com/go/aem_cmp_tech_form_options_v2_jp) | 複数オプション入力フィールド | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [フォーム非表示](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_jp) | 非表示の入力フィールド | `/libs/foundation/components/form/hidden` |
| [フォームボタン](https://adobe.com/go/aem_cmp_tech_form_button_v2_jp) | 送信ボタンまたはカスタムボタン | `/libs/foundation/components/form/submit` |
| [ナビゲーション](https://adobe.com/go/aem_cmp_tech_navigation_v1_jp) | ネストしたページ階層を一覧表示するサイトナビゲーションコンポーネント | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [言語ナビゲーション](https://adobe.com/go/aem_cmp_tech_langnav_v1_jp) | グローバル言語構造を一覧表示する言語および国の切り替え機能 | `-` |
| [クイック検索](https://adobe.com/go/aem_cmp_tech_search_v1_jp) | 結果をドロップダウンメニューでインプレース候補として表示する検索コンポーネント | `/libs/foundation/components/search` |
| [ティーザー](https://adobe.com/go/aem_cmp_tech_teaser_v1_jp) | 画像、タイトル、リッチテキスト、追加コンテンツや他のアクションへのリンクを使用して、コンテンツ作成者が詳細なコンテンツへのティーザーを容易に作成できるようにする | `-` |
| [タブ](https://adobe.com/go/aem_cmp_tech_tabs_v1_jp) | コンテンツ作成者がページコンテンツを複数のタブに整理できるようにする | `-` |
| [カルーセル](https://adobe.com/go/aem_cmp_tech_carousel_v1_jp) | コンテンツ作成者がコンテンツをスライドの回転カルーセルに整理できるようにする | `/libs/foundation/components/carousel` |
| [コンテンツフラグメント](https://adobe.com/go/aem_cmp_tech_cf_v1_jp) | コンテンツフラグメントを表示できるようにする | `-` |
| [コンテンツフラグメントリスト](https://adobe.com/go/aem_cmp_tech_cflist_v1_jp) | コンテンツフラグメントのリストを表示できるようにする | `-` |
| [区切り記号](https://adobe.com/go/aem_cmp_tech_separator_v1_jp) | ページのコンテンツを区切る | `-` |
| [アコーディオン](https://adobe.com/go/aem_cmp_tech_accordion_v1_jp) | 折りたたみ可能なアコーディオンの形式にコンテンツパネルを整理する | `-` |
| [コンテナ](https://adobe.com/go/aem_cmp_tech_container_v1_jp) | コンテナ内のコンポーネントを整理する | `-` |
| [ボタン](https://adobe.com/go/aem_cmp_tech_button_v1_jp) | ページ上にボタンを作成する | `-` |
| [ダウンロード](https://adobe.com/go/aem_cmp_tech_download_v1_jp) | ダウンロード可能なアセットをページに追加する | `-` |
| [エクスペリエンスフラグメント](https://adobe.com/go/aem_cmp_tech_xf_v1_jp) | エクスペリエンスフラグメントをページに追加する | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [埋め込み](https://adobe.com/go/aem_cmp_tech_embed_v1_jp) | ページ内に外部リソースを埋め込む | - |
| [プログレスバー](https://adobe.com/go/aem_cmp_tech_progress_v1) | 目標に対する進捗を視覚的に表現する | - |
| [PDF ビューア](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_jp) | ページに PDF ドキュメントを表示します。 | - |

## コアコンポーネントのアップグレード {#upgrade-of-core-components}

バージョン管理されたコンポーネントのメリットの 1 つは、新しい AEM バージョンへの移行と新しいコンポーネントバージョンへの移行を切り離すことができる点です。また、新しいコンポーネントバージョンが使用可能になった場合は、コンポーネントごとに新バージョンへ個別に移行できます。

コアコンポーネントのバージョンが移行先の新しい AEM バージョンもサポートしている場合、新しい AEM バージョンへの移行はコアコンポーネントの動作に影響を与えません。[廃止または削除](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=ja)された API を使用していない限り、コアコンポーネントのカスタマイズ部分も影響を受けません。

コアコンポーネントを新しいバージョンに移行しても、コンポーネントの動作には影響しませんが、ページ作成者向けの新しい機能が導入されることはあります。これらの機能については、デフォルトの動作が望ましくない場合、テンプレートエディターで何らかの設定が必要になる可能性があります。一方、カスタマイズ部分は適合が必要になる可能性があります。詳しくは、[コアコンポーネントのカスタマイズ](customizing.md#upgrade-compatibility-of-customizations)を参照してください。
