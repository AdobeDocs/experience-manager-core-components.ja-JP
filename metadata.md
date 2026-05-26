---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8id: c45915cf-e157-4af7-a80d-97b905bcb3a5
usetq: true
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Adobe Experience Manager コアコンポーネントのドキュメント
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.en
index: true
recommendations: noDisplay
source-git-commit: 46e65d8dc8f5229e233747ffebe219734ec61adf
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 1%

---


# 内部使用のためのメタデータ

GitHub オーサリングシステムのメタデータは階層であり、次のレベルの前例で定義されています。

1. metadata.md
1. ToC
1. 記事

metadata.md ファイルで定義されたメタデータは、リポジトリ全体に適用されますが、ToC レベルとアーティクルレベルで上書きできます。 メタデータの上書きは、可能な限り低いレベルで行う必要があります。

experience-manager-core-components.en リポジトリのメタデータは、必要な最小値です。

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

記事

* `title`
* `description`
* `index: false` （以前のバージョンのコンポーネントのみ）

メタデータに関する追加情報については、[社内オーサリングガイド ](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)を参照してください。
