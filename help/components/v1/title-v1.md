---
title: タイトルコンポーネント（v1）
description: コアコンポーネントのタイトルコンポーネントは、インプレース編集機能を備えたセクション見出しコンポーネントです。
index: false
role: Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
TQID: https://experienceleague.adobe.com/pctqDaQdDE13Md5ubCounfF-7u7r7dha-wzLB20kLjQ
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 100%

---

# タイトルコンポーネント（v1） {#title-component-v}

コアコンポーネントのタイトルコンポーネントは、インプレース編集機能を備えたセクション見出しコンポーネントです。

## 使用方法 {#usage}

タイトルコンポーネントは、コンテンツのセクションのタイトルまたは見出しとして使用するためのものです。

使用可能な見出しレベルは、[デザインダイアログ](#design-dialog)でテンプレート作成者が定義できます。 コンテンツ編集者は、[編集ダイアログ](#edit-dialog)で、使用可能な見出しレベルから選択できます。 利便性の向上のため、見出しテキストの簡単なインプレース編集も可能です。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、AEM 6.3 に付属しているコアコンポーネントのリリース 1.0.0 で最初に導入されたタイトルコンポーネント v1 について説明します。

タイトルコンポーネント v1 の互換性を次の表に示します。

| AEM のバージョン | タイトルコンポーネント v1 |
|--- |--- |
| 6.3 | 互換性あり |
| 6.4 | 互換性あり |

>[!CAUTION]
>
>このドキュメントでは、タイトルコンポーネント v1 について説明します。
>
>タイトルコンポーネントの現在のバージョンについて詳しくは、[タイトルコンポーネント](/help/components/title.md)のドキュメントを参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

以下は [We.Retail](https://helpx.adobe.com/jp/experience-manager/6-4/sites/developing/using/we-retail.html) から取得したサンプルです。

### スクリーンショット {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>コアコンポーネントからの JSON エクスポートには、コアコンポーネントのリリース 1.1.0 が必要です。 詳しくは、[コアコンポーネント v1 の互換性情報](/help/versions.md)を参照してください。

## 編集ダイアログ {#edit-dialog}

編集ダイアログでは、コンテンツ作成者がタイトルテキストを定義したり、見出しレベルを選択したりできます。

>[!NOTE]
>
>タイトルの値を空にすると、ページタイトルが表示されます。

![](/help/assets/chlimage_1-91.png)

インプレースエディターを使用して、タイトルコンポーネントのテキストを編集することもできます。

![](/help/assets/chlimage_1-37.png)

## デザインダイアログ {#design-dialog}

デザインダイアログでは、コンテンツ作成者が使用する際のタイトルコンポーネントのデフォルト見出しレベルをテンプレート作成者が定義できます。

![](/help/assets/chlimage_1-92.png)

## 技術的詳細 {#technical-details}

タイトルコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title) を参照してください。

コアコンポーネントプロジェクト全体を GitHub からダウンロードできます。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。
