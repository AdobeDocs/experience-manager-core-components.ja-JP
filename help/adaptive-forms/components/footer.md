---
title: アダプティブフォームのコアコンポーネント - フッター
description: アダプティブフォームのフッターコアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '769'
ht-degree: 100%

---

# フッター {#footer-adaptive-forms-core-component}

通常、アダプティブフォームのフッターコンポーネントはフォームの下部に表示される領域であり、著作権表示、関連リソースへのリンク、連絡先情報などの情報が含まれます。 フッターでは、最後の更新日などの追加情報を提供できます。これは、アクセシビリティのニーズを持つユーザーにとって役立ちます。

**例**

![例](/help/adaptive-forms/assets/footer.png)

## 使用方法 {#reasons-to-use-footer}

フッターコンポーネントをフォームに含める方がメリットが大きい理由は、次のようにいくつかあります。

- **法的要件**：一部のフォームには、免責事項、著作権表示、またはその他の法的事項を含める必要が生じる場合があります。 フッターは、こうした情報を含めるのに便利な場所です。

- **ナビゲーション**：プライバシーポリシー、利用規約、連絡先ページなど、web サイト上の重要なページへのリンクを表示できます。

- **ブランディング**：ロゴなどのブランディング要素を表示して、組織や web サイトのアイデンティティを強化できます。

- **一貫性**：フォームのデザインとレイアウトの一貫性が維持され、ユーザーがよりフォームを直感的かつ簡単に移動できるようになります。

- **追加のコンテキスト**：フォームについて説明するテキストや関連リソースへのリンクなど、フォームに追加のコンテキストを提供し、フォームをよりわかりやすく使いやすいものにすることができます。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームのフッターコアコンポーネントは、Cloud Service 向けコアコンポーネント 2.0.4 および AEM 6.5.16.0 Forms 以降向けコアコンポーネント 1.1.12 の一部として、2023年2月にリリースされました。次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | <br>[リリース 1.1.12](/help/adaptive-forms/version.md) 以降、2.0.0 未満と互換性があります。 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 技術的詳細 {#technical-details}

アダプティブフォームのフッターコアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。


## 設定ダイアログ {#configure-dialog}

設定ダイアログを使用すると、訪問者のフッターエクスペリエンスを簡単にカスタマイズできます。また、簡単にフッターのオプションを定義して、シームレスなユーザーエクスペリエンスを実現することもできます。

![「プロパティ」タブ](/help/adaptive-forms/assets/footer_propertiestab.png)

- **「編集ダイアログ」ボックス**
「編集ダイアログ」には、ユーザーがフッターのテキストを作成できる、標準のリッチテキスト形式のツールが用意されています。

- **太字** - 選択したテキストやカーソルの後の入力したテキストを太字にすることができます。`Ctrl+B` は、キーボードショートカットです。

- **斜体** - 選択したテキストやカーソルの後の入力したテキストを斜体にすることができます。`Ctrl+I` は、キーボードショートカットです。

![「箇条書き」オプション](/help/adaptive-forms/assets/footer_bullet.png)


- **箇条書き**

   - **箇条書きアイコン** - 選択したテキストを箇条書きリストとして書式設定するか、カーソルの後に箇条書きリストを挿入するために使用します。箇条書きリストを終了するには、「箇条書き」ボタンをタップまたはクリックするか、キャリッジリターンを 2 回入力します。

   - **番号付きリストアイコン** - 選択したテキストを番号付きリストとして書式設定するか、カーソルの後に番号付きリストを挿入するために使用します。番号付きリストを終了するには、「番号付き」ボタンをタップまたはクリックするか、キャリッジリターンを 2 回入力します。

   - **アウトデントアイコン** - 選択したテキストまたはカーソルの後の入力テキストのインデントレベルを減らします。選択したテキストまたはカーソルの位置が既にインデントされている場合にのみ有効です。

   - **インデントアイコン** - 選択したテキストまたはカーソルの後の入力テキストのインデントレベルを増やします。

![「ハイパーリンク」オプション](/help/adaptive-forms/assets/footer_link.png)

- **ハイパーリンク**

   - **パス** - パスを入力します
      1. 選択を開くダイアログを使用して、AEM 内のパスを選択します。
      1. リンクが AEM 内ではない場合は、絶対 URL を入力します。
      1. 絶対パス以外は、AEM を基準とした相対パスとして解釈されます.

   - **代替テキスト** - リンクの説明用代替テキストを入力します。

   - **ターゲット** - リンクの動作を選択します。
      - ターゲット
      - 同じタブ
      - 新しいタブ
      - 親フレーム
      - トップフレーム

   - **リンク解除アイコン** - このオプションを選択すると、選択したテキストに適用されているリンクが削除されます。このオプションは、リンクが既に選択されている場合にのみ有効です。

   - **段落形式アイコン** - このオプションを使用すると、選択したテキストに段落形式を適用できます。また、カーソルの後に挿入するテキストの書式を設定することもできます。タイトルの見出しレベルを定義します。

- **ID**：このオプションでは、HTML 内およびデータレイヤー内のコンポーネントの一意の ID を制御できます。

   - 空白のままにした場合は、一意の ID が自動的に生成されます。生成された ID は結果のページで確認できます。
   - ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   - ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}
