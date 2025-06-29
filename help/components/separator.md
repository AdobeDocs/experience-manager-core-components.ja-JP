---
title: セパレーターコンポーネント
description: セパレーターコンポーネントは、ページ上のコンポーネント間に区切りを作成します
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '306'
ht-degree: 100%

---


# セパレーターコンポーネント {#separator-component}

コアコンポーネントのセパレーターコンポーネントは、コンテンツを区切るための横罫線を表示します。

{{traditional-aem}}

## 使用方法 {#usage}

セパレーターコンポーネントを使用すれば、コンテンツ間の区切りとして横罫線を手軽に作成して、ページ上の情報をうまく整理できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、セパレーターコンポーネントの現在のバージョン（2019年2月にコアコンポーネントのリリース 2.3.0 で導入された v1）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | <br>[リリース 2.17.4](/help/versions.md) 以前と互換性あり | 互換性あり | 互換性あり | 互換性あり |

## コンポーネント出力のサンプル {#sample-component-output}

セパレーターコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_separator_jp)を参照してください。

### 技術的詳細 {#technical-details}

セパレーターコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

![セパレーターコンポーネントの編集ダイアログ](/help/assets/separator-edit.png)

* **ID** - このオプションを使用すると、HTML 内および [データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、セパレーターコンポーネントに適用するスタイルをテンプレート作成者が定義できます。

### 「スタイル」タブ {#styles-tab}

セパレーターコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。
