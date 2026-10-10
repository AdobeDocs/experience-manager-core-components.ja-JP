---
title: アドビクライアントデータレイヤーの拡張
description: アドビクライアントデータレイヤーは、いくつかの基本的なパターンに従って拡張できます
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: 'https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE'
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: d9d38edd-df1b-480c-8f5e-72b62576f390
    internal-label: Site and page features
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
subfeature_v2:
  - id: c43ff1f6-5a6d-4e8c-b3cc-6bdb3fa6e092
    internal-label: Core components
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
    internal-label: Adobe Client Data Layer
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 025b8134f7675b4515f4586910a94a2732bfa2ee
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%
---
# アドビクライアントデータレイヤーの拡張 {#extending-acdl}

コアコンポーネントは、カスタムダイアログオプションで拡張できます。このオプションを使用すると、コンテンツ作成者はデータレイヤーに関連する追加情報を入力できます。

これらのフィールドをコアコンポーネントが提供するデータレイヤーに含めるには、独自のデータレイヤーメソッドを実装するコンポーネントのモデルを拡張する必要があります。

## 例：タイトルコンポーネント {#example}

[タイトルコンポーネント](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)などのコアコンポーネントは、デフォルトで [`ComponentData`](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java) を返す `getData` メソッドを持つ[コンポーネント](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)を拡張します。

`ComponentData` は、コンポーネントが実装できる事前定義済みのフィールド（[`TitleImpl`](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java) に対して `getDataLayerLinkUrl` や `getDataLayerTitle` など）をシリアル化します。

したがって、カスタム Sling モデルには、より多くのフィールドを返すように `ComponentData` を拡張するオブジェクトを返す `getData` メソッドがある場合があります。

これにより、データレイヤーに入力されるデータの JSON を使用して、コンポーネントの HTML 要素に `data-cmp-data-layer` 属性が追加されます。 この時点で、このデータまたは関連するイベントをリッスンするスクリプトを実装できます。

>[!TIP]
>
>データレイヤーの柔軟性をさらに詳しく調べるには、カスタムコンポーネントでデータレイヤーを有効にする方法などの統合オプションについて確認してください。
