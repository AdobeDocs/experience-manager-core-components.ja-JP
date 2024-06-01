---
title: AEM Adaptive Formsのキャプチャ
description: hCaptcha&reg; サービスを使用してフォームのセキュリティを簡単に強化します。 ステップバイステップガイドをご用意しております。
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: ddfd55259f84443e6add3ced09fd319bcd9c1677
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 17%

---

# Captcha コンポーネント{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> この機能は早期導入プログラムの下にあります。 早期導入プログラムに参加し、機能へのアクセスをリクエストするには、公式メール ID から aem-forms-ea@adobe.com にメールを送信してください。</span>

hCaptcha® サービスは、ボット、スパム、自動不正使用からフォームを保護します。 チェックボックスウィジェットの課題を設定し、ユーザーの応答を評価して、フォームを操作しているのが人間かボットかを判断します。 これにより、テストが失敗した場合にユーザーが続行するのを防ぎ、ボットがスパムや悪意のあるアクティビティを投稿するのを防ぐことにより、オンライントランザクションを安全にすることができます。

![H キャプチャ®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## 使用方法 {#usage}

フォーム送信プロセスに hCaptcha チャレンジを含める方がメリットが大きい理由はいくつかあります。以下に例を示します。

- **ボットの防止**：これにより、フォームが人間によって送信されるので、スパムと自動送信が減少します。

- **セキュリティ**：セキュリティのレイヤーが追加され、各フォーム送信の正当性が検証され、悪意のある攻撃から保護されます。

- **データの整合性**：複数の送信や不正な送信を防ぐことにより、フォームを通じて収集されるデータの整合性と正確性を維持するのに役立ちます。

- **ユーザーの検証**：フォームを送信するユーザーの ID を確認し、認証済みのユーザーのみが機密トランザクションを完了できるようにします。

- **読み込み管理**：フォーム送信率を制御し、トラフィックが多い期間中のシステム過負荷を防ぐことで、サーバー負荷の管理に役立ちます。

## 技術的詳細 {#technical-details}

Captcha コンポーネントの最新情報については、のテクニカルドキュメントをご覧ください。 [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). コアコンポーネントの開発について詳しくは、 [コアコンポーネント開発者向けのドキュメント](/help/developing/overview.md)をご覧ください。

を使用して、hCaptcha コンポーネントのプロパティを指定します。 [設定ダイアログ](#configure-dialog). 設定ダイアログは、フォームのオーサリングを容易にし、複雑なフォームを効率的に作成するために構築されるコアコンポーネントの一部です。

## バージョンと互換性 {#version-and-compatibility}


アダプティブForms hCaptcha コンポーネントは、 [コアコンポーネント 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). 次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

|  |  |
|---|---|
| コンポーネントのバージョン | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | 互換性あり | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

## 設定ダイアログ {#configure-dialog}

Captcha コンポーネントのプロパティは、設定ダイアログで簡単にカスタマイズできます。このダイアログには、「基本」タブと「検証」タブがあり、様々なプロパティをカスタマイズできます。

### 「基本」タブ {#basic-tab}

- **[!UICONTROL 名前]:** Captcha コンポーネントの名前を指定すると、フォーム内とルールエディター内の両方で一意の名前を使用して、フォームコンポーネントを簡単に識別できます。
- **[!UICONTROL タイトル]:** Captcha コンポーネントのタイトルを指定します。
- **[!UICONTROL 設定]:** hCaptcha® 用に設定したクラウド設定を選択します。
- **Captcha サイズ：** hCaptcha® チャレンジダイアログボックスの表示サイズを選択できます。 の使用 **[!UICONTROL コンパクト]** 小さいサイズのを表示するオプション **[!UICONTROL 標準]** 比較的大きなサイズの hCaptcha® チャレンジダイアログを表示するオプション。<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![「Captcha 基本」タブ](/help/adaptive-forms/assets/hcaptcha-basic.png)

### 「検証」タブ {#validation-tab}

- **[!UICONTROL 検証メッセージ]:** フォーム送信時に Captcha 検証の検証メッセージを指定します。
- **[!UICONTROL スクリプト検証メッセージ]** - スクリプトの検証が失敗した場合にプロンプト・メッセージを入力するには、このオプションを使用します。

  ![「Captcha 検証」タブ](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® は、Intuition Machines, Inc.の登録商標です。**

**詳しく見る** その他について **Captcha コンポーネント** サービス（例：）

- [コアコンポーネント用アダプティブフォームでの Captcha の使用](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [基盤コンポーネント用アダプティブフォームでの Captcha の使用](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [基盤コンポーネント用のアダプティブフォームでの自動 CAPTCHA の使用](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [基盤コンポーネント用のアダプティブフォームでのGoogle reCAPTCHA の使用](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}
