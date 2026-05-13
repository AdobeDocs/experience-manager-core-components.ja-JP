---
title: コアコンポーネントのレスポンシブデザイン
description: コアコンポーネントのレスポンシブデザインと、コアコンポーネントがプロジェクトに与える影響について説明します。
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 100%

---

# コアコンポーネントのレスポンシブデザイン {#responsive-design}

すべてのコアコンポーネントは、完全にレスポンシブに動作するように設計されており、デバイス間のシームレスなエクスペリエンスを実現します。 例えば、[カルーセル、](/help/components/carousel.md)[タブ、](/help/components/tabs.md)および[アコーディオンコンポーネント](/help/components/accordion.md)などの高度なコンポーネントは、すべての状況で応答性を維持するために、実装プロジェクトのコンテキスト内で特定の検討を必要とする場合があることに注意することが重要です。

これらのコンポーネントは応答動作を多様に示すことができ、そしてコアコンポーネントを標準で軽量に保つというアドビのコミットメントに基づき、詳細なレスポンシブ側面を実装するように意図的にプロジェクトに残されています。

例えば、狭い画面では、タブコンポーネントは、幅の広いタブを新しい行に分割したり、垂直スクロールを許可したり、タブをドロップダウンに変換したり、アコーディオンスタイルを採用したりすることで適応できます。 これらの動作をすべて実装するとパフォーマンスに影響が及ぶ可能性があるので、[clientlibs](/help/developing/including-clientlibs.md#provided) は、完全なソリューションではなく、実装する際の出発点として意図されています。
