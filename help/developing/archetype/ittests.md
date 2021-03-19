---
title: AEM プロジェクトアーキタイプの it.tests モジュール
description: AEM プロジェクトアーキタイプの統合テストの使用方法
feature: コアコンポーネント、AEMプロジェクトアーキタイプ
role: アーキテクト、開発者、管理者
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 90%

---


# AEM プロジェクトアーキタイプの it.tests モジュール {#ittests-module}

プロジェクトには、次の 3 つのレベルのテストが含まれています。

* [単体テスト](core.md#unit-tests)
* 統合テスト
* [UI テスト](uitests.md)

この記事では、it.tests モジュールの一部として使用できる統合テストについて説明します。

## 統合テストの実行 {#running-tests}

サーバーサイドの統合テストを使用すると、AEM 環境（AEM サーバー上など）でユニット型のテストを実行できます。テストするには、次のコマンドを実行します。

```
mvn clean verify -PintegrationTests
```