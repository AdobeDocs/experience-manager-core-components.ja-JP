---
title: 統合とアドビクライアントデータレイヤー
description: アドビクライアントデータレイヤーとカスタムコンポーネントの統合方法のほか、Adobe Analytics や Adobe Target との統合が web サイトに対するインサイトの取得にどう役に立つかを説明します。
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
TQID: https://experienceleague.adobe.com/xncfOtz1FNyeH6CjQjg7cSeIonIg2mkBIPUgZvMI7Ww
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: ae478996-b206-4712-9b0c-dc78a2644453id: d429a63e-ade4-4117-b04e-9b996d1c94ef
subfeature_v2: id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 100%

---

# アドビクライアントデータレイヤーとの統合 {#integrations}

アドビクライアントデータレイヤーは、あらゆるスクリプトのあらゆる種類のデータを表示および利用できる標準化された方法を提供し、web サイトを実装する際の手間を軽減します。

アドビクライアントデータレイヤーはカスタムコンポーネントと統合でき、web サイトに対するインサイトを取得するうえで Adobe Analytics や Adobe Target との統合が役に立ちます。

## カスタムコンポーネントへのデータレイヤーの有効化 {#enabling-custom-components}

カスタムコンポーネントをデータレイヤーに自動的に追加するには：

1. 追跡する必要があるカスタムコンポーネントモデルのプロパティを定義します。
1. カスタムコンポーネントの HTL に `data-cmp-data-layer` 属性を追加します。例： `data-cmp-data-layer="${mycomponent.data.json}"`.

カスタムコンポーネントの特定の要素がクリックされるたびにデータレイヤーに `cmp:click` イベントを自動的にトリガーさせるには、カスタムコンポーネントの HTL で追跡の対象となる要素に `data-cmp-clickable` 属性を追加します。

`data-cmp-data-layer-enabled` 属性をクライアント側で照会して、データレイヤーが有効かどうかを確認できます。

>[!TIP]
>
>Adobe Client Data Layer とコアコンポーネントの統合に関する技術的な詳細と、カスタムコンポーネントでデータレイヤーを有効にする方法については、コアコンポーネントリポジトリの [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) ファイルを参照してください。

## Adobe Analytics や Adobe Target との統合 {#analytics-target}

Adobe Analytics や Adobe Target との組み合わせることで、アドビクライアントデータレイヤーは非常に強力で柔軟なツールセットの基盤となり、デジタルエクスペリエンスのインサイトを獲得することができます。 次のチュートリアルでは、サンプル統合の手順を説明します。

### Adobe Analytics でページデータを収集 {#collect-page-data}

アドビクライアントデータレイヤーのビルトインの機能と AEM コアコンポーネントを使用して、Adobe Experience Manager Sites のページに関するデータを収集する方法を説明します。 Experience Platform Launch と Adobe Analytics 拡張は、ルールを作成して Adobe Analytics にページデータを送信するために使用されます。

[こちらのチュートリアルをご覧ください。](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html?lang=ja)

### Adobe Analytics を使用してクリックされたコンポーネントを追跡 {#track-clicked-components}

イベント駆動型のアドビクライアントデータレイヤーを AEM コアコンポーネントと共に使用して、Adobe Experience Manager サイト上にある特定のコンポーネントのクリックを追跡します。 Experience Platform Launch でルールを使用して、クリックイベントをリッスンし、コンポーネントでフィルタリングして、リンクのトラックビーコンと共にデータを Adobe Analytics に送信する方法について説明します。

[こちらのチュートリアルをご覧ください。](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html?lang=ja)
