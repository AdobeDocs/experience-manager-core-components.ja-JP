---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Adobe Experience Manager コアコンポーネントのドキュメント
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.ja-JP
index: true
recommendations: noDisplay
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# 内部使用のメタデータ

GitHub オーサリングシステムのメタデータは階層的で、次の高レベルの前例として定義されています。

1. metadata.md
1. から C
1. 記事

metadata.md ファイルで定義されたメタデータはリポジトリ全体に適用されますが、目次と記事のレベルで上書きできます。 メタデータの上書きは、できるだけ低いレベルで行う必要があります。

最低限必要なのは、experience-manager-core-components.en リポジトリ内のメタデータです。

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

メタデータに関する追加情報については、[&#x200B; 内部オーサリングガイド &#x200B;](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution) を参照してください。
