---
title: アダプティブフォームのコアコンポーネント - 画像
description: アダプティブフォームの画像コアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '1058'
ht-degree: 100%

---

# 画像コンポーネント{#image-adaptive-forms-core-component}

アダプティブフォームの画像コンポーネントでは、フォームに画像を含めることができます。これらの画像を使用して、フォームの全体的なデザインを引き立てたり、追加情報を提供したり、ユーザーがフォームの目的を理解できるように視覚的な要素として機能させたりすることができます。画像コンポーネントを使用して、フォームにロゴ、写真またはグラフィックを追加できます。

アクセシビリティについては、視覚に障害があるユーザーのために、**代替テキスト**&#x200B;を画像に追加して、画像に代わる短い説明文を指定することが重要です。

**例**

![例](/help/adaptive-forms/assets/image.png)


## 使用方法 {#reasons-to-use-image-in-a-form}

アダプティブフォームに画像コンポーネントを含める方がメリットが大きい理由は、次のようにいくつかあります。

- **ブランディング**：フォームを作成した組織のロゴや名前を表示することで、ブランドの認知度を上げ、信頼性を確立するのに役立ちます。

- **視覚要素**：画像は、ユーザーがフォームの目的を理解するのに役立つ視覚的な要素として機能し、ユーザーに追加情報を提供できます。

- **装飾**：フォームの全体的なデザインをより魅力的なものにすることができます。

- **ユーザーエクスペリエンス**：ユーザーがフォームフィールドにアクセスして入力する際に明確で直感的な方法を提供することで、フォームをより使いやすいものにすることができます。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームの画像コアコンポーネントは、Cloud Service 向けコアコンポーネント 2.0.4 および AEM 6.5.16.0 Forms 以降向けコアコンポーネント 1.1.12 の一部として、2023年2月にリリースされました。次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | <br>[リリース 1.1.12](/help/adaptive-forms/version.md) 以降、2.0.0 未満と互換性があります。 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_jp). -->

## 技術的詳細 {#technical-details}

アダプティブフォームの画像コアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。


## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、訪問者の画像エクスペリエンスを簡単にカスタマイズできます。また、簡単に画像オプションを定義して、シームレスなユーザーエクスペリエンスを実現することもできます。

![「プロパティ」タブ](/help/adaptive-forms/assets/image_properties.png)

- **名前** - フォームコンポーネントは、フォーム内とルールエディター内の両方で一意の名前で簡単に識別できますが、名前にスペースや特殊文字を含めることはできません。

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの上にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。

- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **説明** - 説明とは、特定の画像の目的に関する追加情報や説明を提供する簡単な説明文です。

- **ここにアセットをドロップ、またはアップロードするファイルを参照** - このオプションでは、マウスのドラッグ＆ドロップ操作で画像などのアセットをドロップできます。また、「**参照**」ボタンを使って、ローカルのファイルシステムからファイルをアップロードすることもできます。画像を追加すると、画像の下部に 3 つのボタンが表示されます。
   - **編集** - アセットエディターでアセットのレンディションを管理するには、「**編集**」をタップまたはクリックします。
   - **消去** - 現在選択されている画像を選択解除するには、「**消去**」をタップまたはクリックします。
   - **選択** - アセットフォルダーから別の画像を選択するには、「**選択**」オプションをタップまたはクリックします。

- **代替テキスト** - このオプションは、視覚に障害のあるユーザー向けに、画像の代わりとなる短い説明文を入力するために使用されます。

- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## デザインダイアログ {#design-dialog}

デザインダイアログでは、画像コンポーネントの CSS スタイルを定義および管理できます。

### 「スタイル」タブ {#styles-tab}

タブを使用して、コンポーネントの CSS スタイルの定義と管理を行います。アダプティブフォームの画像コアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![デザインダイアログ](/help/adaptive-forms/assets/checkbox-style.png)

- **デフォルトの CSS クラス**：アダプティブフォームの画像コアコンポーネントのデフォルト CSS クラスを指定できます。

- **許可されたスタイル**：スタイルを表す名前と CSS クラスを指定してスタイルを定義します。例えば、「bold text」という名前のスタイルを作成し、CSS クラス「font-weight: bold」を指定できます。 アダプティブフォームエディターでアダプティブフォームにこれらのスタイルを使用または適用できます。 スタイルを適用するには、アダプティブフォームエディターでスタイルを適用するコンポーネントを選択し、「プロパティ」ダイアログに移動して「**スタイル**」ドロップダウンリストから希望のスタイルを選択します。 スタイルを更新または変更する必要がある場合は、デザインダイアログに戻り、「スタイル」タブでスタイルを更新して変更を保存します。

### カスタムプロパティ

![カスタムプロパティダイアログ](/help/adaptive-forms/assets/checkbox-customproperties.png)

カスタムプロパティを使用すると、フォームテンプレートを使用してカスタム属性（キーと値のペア）をアダプティブフォームのコアコンポーネントに関連付けることができます。 カスタムプロパティは、コンポーネントのヘッドレスレンディションのプロパティセクションに反映されます。 これにより、カスタム属性値に基づいて適応する動的なフォーム動作を作成できます。 例えば、開発者は、モバイル、デスクトップ、web プラットフォーム上にヘッドレスフォームコンポーネントの様々なレンディションをデザインできるので、幅広いデバイスでのユーザーエクスペリエンスが大幅に向上します。

- **グループ名**：カスタムプロパティグループを識別する名前を指定できます。 複数のカスタムプロパティグループを追加、削除または並べ替えることができます。 カスタムプロパティグループを追加すると、次のオプションが表示されます。

   - **キーと値のペア**：各カスタムプロパティグループの「**追加**」ボタンをクリックすると、複数のカスタムプロパティ名とカスタムプロパティ値を追加できます。

   - **削除**：タップまたはクリックすると、カスタムプロパティ名とカスタムプロパティ値を削除できます。

   - **並べ替え**：タップまたはクリックしてドラッグすると、カスタムプロパティ名とカスタムプロパティ値の順序を並べ替えることができます。

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}