---
title: コンテンツフラグメントリストコンポーネント (v1)
description: コアコンポーネントのコンテンツフラグメントリストコンポーネントを使用すれば、コンテンツフラグメントのリストを表示できます。
role: Architect, Developer, Admin, User
source-git-commit: e5251010ca41025eb2bb56b66164ecf4cc0145c8
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 93%

---


# コンテンツフラグメントリストコンポーネント  (v1) {#content-fragment-list-component}

コアコンポーネントのコンテンツフラグメントリストコンポーネントを使用すれば、[コンテンツフラグメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=ja)のリストを表示できます。

## 使用方法 {#usage}

コアコンポーネントのコンテンツフラグメントリストコンポーネントを使用すれば、コンテンツフラグメントモデルに基づいて[コンテンツフラグメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)のリストをページに組み込むことができます。これは、他のアプリケーションで容易に使用できる[ヘッドレスコンテンツ](https://helpx.adobe.com/jp/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js)を作成する場合に特に便利です。

* リストとそのプロパティは、[設定ダイアログ](#configure-dialog)で選択できます。
* スタイルは、[デザインダイアログ](#design-dialog)でコンポーネントに適用できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、2019 年 5 月にコアコンポーネントのリリース 2.4.0 で導入されたコンテンツフラグメントコンポーネント v1 について説明します。

>[!CAUTION]
>
>このドキュメントでは、コンテンツフラグメントリストコンポーネント v1 について説明します。
>
>コンテンツフラグメントリストコンポーネントの現在のバージョンについて詳しくは、 [コンテンツフラグメントリストコンポーネント](/help/components/content-fragment-list.md) 文書。

## コンポーネント出力のサンプル {#sample-component-output}

コンテンツフラグメントリストコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_cflist_jp)を参照してください。

## 技術的詳細 {#technical-details}

コンテンツフラグメントリストコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、リストを構成するコンテンツフラグメントとそれらのフラグメントを組み込む要素をコンテンツ作成者が定義できます。

### 「プロパティ」タブ

「**プロパティ**」タブでは、リストに含めるコンテンツフラグメントを定義します。主に、選択したコンテンツフラグメントモデルに基づいていますが、他のフィルターオプションも使用できます。

![コンテンツフラグメントリストコンポーネントの編集ダイアログの「プロパティ」タブ](/help/assets/content-fragment-list-properties.png)

* **モデル** - リストの基となるコンテンツフラグメントモデルのパス。
   * デフォルトでは、**モデルパス**&#x200B;として定義された、モデルのすべてのコンテンツフラグメントがリストに含まれます。
* **親パス** - リストを作成する元となる親パス。
   * 選択した&#x200B;**モデルパス**&#x200B;に基づくコンテンツフラグメントが、指定した&#x200B;**親パス**&#x200B;上のフラグメントにフィルタリングされます。
      * フィールドの右側にある「**選択ダイアログを開く**」ボタンをクリックまたはタップして、パスを指定します。
* **タグ** - 指定したタグを持つコンテンツフラグメントのみリストに含まれます。
   * フィールドの右側にある「**選択ダイアログを開く**」ボタンをクリックまたはタップして、タグを指定します。
   * 選択したタグの横にある「X」をクリックまたはタップすれば、そのタグを削除できます。
* **並べ替え順** - リストの並べ替えに使用するコンテンツフラグメントモデルのフィールド
   * 選択できるのは、テキストフィールド（数値、日付、時刻など）のみです。
* **並べ替え順序** - 「**並べ替え順**」フィールドによるリストの並べ替え方法
   * 昇順または降順
* **最大項目数** - リストに表示する項目の最大数
   * 値が指定されない場合は、すべての項目が返されます。
* **ID** - このオプションを使用すると、HTML 内および[データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

>[!NOTE]
>コアコンポーネントのリリース 2.7.0 では、「**並べ替え順**」、「**並べ替え順序**」、「**最大項目数**」の各オプションが導入されました。

### 「エレメント」タブ

（「**最大項目数**」フィールドで制限されない限り）デフォルトでは、コンテンツフラグメントモデルのすべての要素がリストに含まれます。「**エレメント**」タブを使用すると、含める特定の要素を指定できます。

![コンテンツフラグメントリストコンポーネントの編集ダイアログの「要素」タブ](/help/assets/content-fragment-list-elements.png)

* **エレメント** - 指定したリストに含まれているコンテンツフラグメントの要素のみ表示されます。
   * 「**追加**」ボタンをクリックまたはタップすると、新しい要素を追加できます。
   * 「**削除**」ボタンをクリックまたはタップすると、選択した要素を削除できます。
   * 「**順序**」ハンドルをドラッグすると、要素の順序を並べ替えることができます。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、コンテンツフラグメントリストコンポーネントに適用するスタイルをテンプレート作成者が定義できます。