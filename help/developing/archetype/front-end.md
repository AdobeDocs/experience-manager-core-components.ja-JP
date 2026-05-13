---
title: AEM プロジェクトアーキタイプを使用したフロントエンド開発
description: AEM プロジェクトアーキタイプの Webpack に基づく専用のフロントエンドビルドメカニズム（オプション）について説明します。
feature: Core Components, AEM Project Archetype
role: Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
TQID: https://experienceleague.adobe.com/OIZesRo9peaI6BNsCSzNJi8BzhRhaOH-KaDw9tefjH4
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 100%

---

# AEM プロジェクトアーキタイプを使用したフロントエンド開発 {#front-end}

AEM プロジェクトのアーキタイプには、Webpack ベースの専用フロントエンドビルドメカニズム（オプション）が含まれています。 このように、ui.frontend モジュールは、JavaScript や CSS ファイルを含む、プロジェクトのすべてのフロントエンドリソースの中心となります。 この便利で柔軟な機能を最大限に活用するには、AEM プロジェクトにフロントエンド開発がどのように適合するかを理解することが重要です。

このドキュメントでは、フロントエンドビルドモジュールの一般的な使用パターンおよびユーザーに与える影響について説明します。 ビルドオプションと技術的な手順について詳しくは、アーキタイプの GitHub リポジトリにあるドキュメントを参照してください。

>[!TIP]
>
>最新の AEM プロジェクトのアーキタイプおよび技術的なドキュメントは、[GitHub を参照してください。](https://github.com/adobe/aem-project-archetype)

## AEM フロントエンドおよびバックエンド開発 {#front-end-back-end}

簡単に言えば、AEM プロジェクトは、2 つの異なる関連部分から成ると考えることができます。

* AEM のロジックを駆動し、Java ライブラリ、OSGi サービスなどを生成するバックエンドの開発
* 結果として作成される Web サイトの表示と動作を促し、JavaScript ライブラリと CSS ライブラリを生成するフロントエンド開発

これらの 2 つの開発プロセスはプロジェクトの異なる部分に焦点を当てているので、バックエンドとフロントエンドの開発が並行して行われる可能性があります。

![フロントエンドワークフロー図](/help/assets/front-end-flow.png)

ただし、作成されるプロジェクトでは、バックエンドとフロントエンドの両方の開発作業の出力を使用する必要があります。

## マークアップの決定 {#determining-markup}

プロジェクトに実装するフロントエンド開発ワークフローに関しては、まずバックエンド開発者とフロントエンド開発者がマークアップに同意する必要があります。 通常、AEM はマークアップを定義し、これがコアコンポーネントで提供されます。 [ただし、必要に応じてカスタマイズできます。](/help/developing/customizing.md#customizing-the-markup)

## 可能なフロントエンド開発ワークフロー {#possible-workflows}

フロントエンドビルドモジュールは、便利で柔軟なツールですが、どのように使用されるすべきかについてはユーザーに任されています。 以下の 2 つは&#x200B;*可能な*&#x200B;使用例ですが、個々のプロジェクトでは他の使用モデルが必要になる場合があります。

### Webpack 静的開発サーバーの使用 {#using-webpack}

Webpack を使用すると、ui.frontend モジュール内の AEM Web ページの静的出力に基づいてスタイルを設定し、開発することができます。

1. ページプレビューモードを使用するか、URL に `wcmmode=disabled` を渡すことによって、AEM でページをプレビューする
1. ui.frontend モジュール内でページソースを表示し、静的 HTML として保存する
1. [Webpack を起動](#webpack-dev-server)して、必要な JavaScript と CSS のスタイル設定と生成を開始する
1. `npm run dev` を実行して clientlib を生成する

このフローでは、AEM 開発者が手順 1 と 2 を実行して、静的 HTML をフロントエンド開発者に渡し、フロントエンド開発者が AEM HTML 出力に基づいて開発をおこなうことができます。

>[!TIP]
>
>また、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_jp)を利用して、各コンポーネントのマークアップ出力のサンプルを取り込み、ページレベルではなくコンポーネントレベルで作業することもできます。

### Storybook の使用 {#using-storybook}

[Storybook ](https://storybook.js.org)を使用すると、よりアトミックなフロントエンド開発を実行できます。 Storybook は AEM プロジェクトのアーキタイプには含まれていませんが、Storybook をインストールすると、ui.frontend モジュール内に Storybook アーティファクトを保存することができます。 AEM 内でテストをおこなう準備が整ったら、`npm run dev` を実行して Storybook を clientlib としてデプロイできます。

>[!NOTE]
>
>[Storybook](https://storybook.js.org) は AEM プロジェクトのアーキタイプには含まれていません。 使用する場合は、個別にインストールする必要があります。

## ClientLibs の概要 {#clientlibs}

フロントエンドモジュールは、[AEM clientlib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=ja) を使用して提供されます。NPM ビルドスクリプトを実行する場合、アプリケーションがビルドされ、`aem-clientlib-generator` パッケージがビルド出力結果を取得して、そのような clientlib に変換します。

ClientLib は、次のファイルとディレクトリで構成されます。

* `css/`：HTML で要求できる CSS ファイル
* `css.txt`：ファイルを結合できるように、`css/` 内のファイルの順序と名前を AEM に指示します。
* `js/`：HTML で要求できる JavaScript ファイル
* `js.txt`：ファイルを結合できるように、`js/` 内のファイルの順序と名前を AEM に指示します。
* `resources/`：ソースマップ、非エントリポイントコードチャンク（コード分割による）、静的アセット（アイコンなど）など。

>[!TIP]
>
>AEM での ClientLib の処理方法について詳しくは、[AEM 開発ドキュメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=ja)を、それらをどのように含めるかについて詳しくは、[コアコンポーネントのドキュメント](/help/developing/including-clientlibs.md)を参照してください。
