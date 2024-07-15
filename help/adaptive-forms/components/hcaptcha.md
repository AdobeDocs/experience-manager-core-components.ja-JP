---
title: AEM アダプティブフォームの hCaptcha
description: hCaptcha® サービスでフォームのセキュリティを容易に強化できます。ステップバイステップガイドをご用意しております。
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: 4b05fb9d8db515289095f4d3c6a4efbe872dbde5
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---

# hCaptcha コンポーネント{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview">この機能は早期導入プログラムに基づいています。早期導入プログラムに参加し、機能へのアクセスをリクエストするには、公式メール ID から aem-forms-ea@adobe.com にメールを送信してください。</span>

hCaptcha® サービスは、ボット、スパム、自動化された不正使用からフォームを保護します。チェックボックスウィジェットテストを行ってユーザーの反応を評価し、フォームを使用しているのが人間かボットかを判断します。テストが失敗した場合の続行を防ぎ、ボットによるスパムの投稿や悪意のあるアクティビティを防止することで、オンライントランザクションの安全性を高めます。

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## 使用方法 {#usage}

hCaptcha テストをフォーム送信プロセスに含める方がメリットが大きい理由は、次のようにいくつかあります。

- **ボット防止**：フォームが人間によって送信されていることを確認し、スパムや自動送信を削減します。

- **セキュリティ**：セキュリティのレイヤーを追加し、各フォーム送信の正当性を検証し、悪意のある攻撃から保護します。

- **データの整合性**：複数の送信や不正な送信を防ぐことで、フォームを通じて収集されたデータの整合性と正確性を維持するのに役立ちます。

- **ユーザーの検証**：フォームを送信するユーザーの ID を検証し、認証済みのユーザーのみが機密性の高いトランザクションを完了できるようにします。

- **負荷管理**：フォームの送信レートを制御し、トラフィックが集中する期間にシステムが過負荷になるのを防ぐことで、サーバーの負荷管理に役立ちます。

## 技術的詳細 {#technical-details}

hCaptcha コンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、 [コアコンポーネント開発者向けのドキュメント](/help/developing/overview.md)をご覧ください。

[設定ダイアログ](#configure-dialog)を使用して、hCaptcha コンポーネントのプロパティを指定します。設定ダイアログは、コアコンポーネントの一部です。このコンポーネントは、フォームのオーサリングを容易にし、複雑なフォームを効率的に作成するために構築されています。

## バージョンと互換性 {#version-and-compatibility}


アダプティブフォームの hCaptcha コンポーネントは、[コアコンポーネント 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491) の一部として 2024年5月にリリースされます。次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

|  |  |
|---|---|
| コンポーネントのバージョン | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | 互換性あり | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

## 設定ダイアログ {#configure-dialog}

hCaptcha コンポーネントのプロパティは、様々なプロパティをカスタマイズするための「基本」タブと「検証」タブを含む設定ダイアログを使用して、簡単にカスタマイズできます。

### 「基本」タブ {#basic-tab}

- **[!UICONTROL 名前]：** hCaptcha コンポーネントの名前を指定すると、フォームとルールエディターの両方で一意の名前を使用してフォームコンポーネントを簡単に識別できます。
- **[!UICONTROL タイトル]：** hCaptcha コンポーネントのタイトルを指定します。
- **[!UICONTROL 設定]：** hCaptcha® 用に設定されたクラウド設定を選択します。
- **Captcha サイズ：** hCaptcha® テストダイアログボックスの表示サイズを選択できます。「**[!UICONTROL コンパクト]**」オプションを選択すると小さいサイズ、「**[!UICONTROL 標準]**」オプションを選択すると比較的大きなサイズの hCaptcha® テストダイアログを表示できます。<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![hCaptcha の「基本」タブ](/help/adaptive-forms/assets/hcaptcha-basic.png)

### 「検証」タブ {#validation-tab}

- **[!UICONTROL 検証メッセージ]：**&#x200B;フォーム送信時の Captcha 検証の検証メッセージを指定します。
- **[!UICONTROL スクリプト検証メッセージ]** - このオプションを使用して、スクリプトの検証が失敗した場合にプロンプトメッセージを入力します。

  ![hCaptcha の「検証」タブ](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® は、Intuition Machines, Inc. の登録商標です。**

他の **Captcha コンポーネント**&#x200B;とそのサービスについて&#x200B;**詳しく**&#x200B;は、以下を参照してください。

- [コアコンポーネントのアダプティブフォームでの hCaptcha の使用](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [基盤コンポーネントのアダプティブフォームでの hCaptcha の使用](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [基盤コンポーネントのアダプティブフォームでの Turnstile Captcha の使用](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [基盤コンポーネントのアダプティブフォームでの Google reCAPTCHA の使用](https://experienceleague.adobe.com//docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}
