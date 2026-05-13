---
title: メールコアコンポーネントの概要
description: メールコアコンポーネントの柔軟性を利用して、説得力のあるメールコンテンツを作成し、Adobe Campaign の機能を活用して提供します。
role: Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
index: false
TQID: https://experienceleague.adobe.com/PLDfeItW57FUgvSUO7kHgeNP8KogBwVA2AeEd-srbwg
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: ae478996-b206-4712-9b0c-dc78a2644453id: d429a63e-ade4-4117-b04e-9b996d1c94efid: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
subfeature_v2: id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 439
ht-degree: 100%

---

# メールコアコンポーネントの概要 {#email-core-components-introduction}

メールコアコンポーネントの柔軟性を利用して、説得力のあるメールコンテンツを作成し、Adobe Campaign の機能を活用して提供します。

## 概要 {#overview}

メールコアコンポーネントは、コアコンポーネントと同一の強力な基盤上に構築されています。 メールコンテンツをシンプルで柔軟なドラッグ＆ドロップでオーサリングでき、Adobe Campaign の機能を使用してオーディエンスに配信できます。

## メリット {#benefits}

メールは、ブランドエクスペリエンスとカスタマージャーニーの一部です。 メールコアコンポーネントを使用すると、作成者は AEM 内からメールコンテンツを作成でき、一貫したブランドのエクスペリエンスを提供し、コンテンツベロシティが向上します。

* コアコンポーネントを使用したページのオーサリングと同様に、メールコアコンポーネントを使用すると、作成者は、技術的な知識がなくても、ブランディングガイドラインに従いながらメールを組み立てることができます。
* アセットやコンテンツを再利用する機能により、作成者はブランディングガイドラインに従い、コンテンツ作成プロセスを最適化することもできます。

## 機能 {#features}

* コアメールコンポーネントは、[コアコンポーネント](/help/introduction.md)に基づいているため、[編集可能なテンプレート](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)および[スタイルシステム](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ja)もサポートしています。
* メールコンテンツを作成するための、[メール用に最適化された、すぐに使用できる 10 個のコンポーネント](#components)があります。
* ほとんどのダイアログフィールドに [Adobe Campaign の変数](campaign-variables.md)が挿入されているので、コアメールコンポーネントは、高度なパーソナライズ機能を提供します。
* 柔軟な[セグメント化コンポーネント](/help/email/components/segmentation.md)を使用すると、コンテンツを詳細にセグメント化することができます。
* コアメールコンポーネントは、[CSS スタイルインライナー](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation)、[HTML フィールド名インライナー](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner)および[HTML サニタイザー](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)によって、メール作成に最適な HTML 出力を提供します。
* メールコンテンツは、`/content` 下の任意の場所で作成できます。
* メールコアコンポーネントは、[オープンソース](https://github.com/adobe/aem-core-email-components)です。

## 要件 {#requirements}

メールコアコンポーネントには、以下の要件があります。

| AEM | Adobe Campaign | コアコンポーネント |
|---|---|---|
| AEM 6.5.14.0+<br>オンプレミスまたは AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [リリース 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Adobe Campaign の統合は AEM as a Cloud Service ではサポートされていないので、メールコアコンポーネントも同様に AEM as a Cloud Service ではサポートされません。

## メールコンポーネント {#components}

メールコアコンポーネントの現在のバージョンには、以下のコンポーネントが含まれています。

* [ページ](components/page.md)
* [コンテナ](components/container.md)
* [タイトル](components/title.md)
* [テキスト](components/text.md)
* [画像](components/image.md)
* [ボタン](components/button.md)
* [ティーザー](components/teaser.md)
* [エクスペリエンスフラグメント](components/experience-fragment.md)
* [コンテンツフラグメント](components/content-fragment.md)
* [セグメント化](components/segmentation.md)

## インストールと使用 {#installation-usage}

メールコアコンポーネントのインストールについて詳しくは、[メールコアコンポーネントの使用](using.md)ドキュメントを参照してください。
