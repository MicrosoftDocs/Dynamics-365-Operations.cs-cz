---
title: Ukázkové šeky dodavatele v elektronickém výkaznictví
description: Toto téma obsahuje obecné informace o použití formátů ukázkových šeků v elektronickém výkaznictví.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 72581a6d852fe6eb5b4ad894027c1f5a3b5363e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250595"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Ukázkové šeky dodavatele v elektronickém výkaznictví

[!include [banner](../includes/banner.md)]

Elektronické výkaznictví můžete použít k formátování šeků dodavatele. Na trhu existuje mnoho formátů šeků specifických pro různé banky a poskytovatele šeků. Do úložiště nástrojů elektronického výkaznictví v modelu platebních šeků byly zahrnuty formáty ukázkových šeků. Tyto ukázkové šeky jsou označeny **Šek uprostřed (USA)** a **Šek nahoře a útržek dole (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Jaké formáty šeků jsou aktuálně podporovány?

Měli byste vždy přejít do knihovny sdíleného majetku ve službě Microsoft Dynamics Lifecycle services (LCS) a zobrazit aktuální seznam dostupných souborů, které mají typ prostředku **konfigurace GER**. Další oddíl "Co musím nastavit?" obsahuje odkaz na téma, které vysvětluje, jak vytvořit úložiště LCS, abyste mohli revidovat dostupné konfigurace a importovat vybrané konfigurace.

Microsoft Dynamics 365 Finance zahrnuje ukázkový formát, kde je šek nahoře, následován dvěma částmi vyplacení. Dále zahrnuje ukázkový formát, kde je šek uprostřed mezi dvěma částmi vyplacení. Tyto ukázkové formáty odpovídají formátům šeků Deluxe business.

## <a name="what-do-i-have-to-set-up"></a>Co je nutné nastavit?

- Před tiskem šeků pomocí elektronického výkaznictví je třeba alespoň jednu aktivní konfiguraci šeku importovat do vašich konfigurací elektronického výkaznictví. Pokyny viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Když konfigurujete šeky pokladny a banky pro bankovní účet, zvolte zaškrtávací políčko **Obecný elektronický formát exportu** a vyberte příslušný formát šeku jako konfiguraci formátu exportu.
- Také musíte určit počet řádků, které budou vytištěny na části pro vyplacení. Ujistěte se, že nazapomenete při výpočtu řádků na řádky záhlaví. Pro dva ukázkové formáty šeků je doporučený počet řádků 17. Toto číslo se však bude měnit v závislosti na vašich zásobách šeků a ovladačích tiskárny.
- Doporučujeme, abyste vytiskli zkušební šeku pro ověření rozvržení šeku. Pro tisk zkušebního šeku vyberte možnost **Tisk testu**. Ukázkové formáty šeku jsou nejlepší tehdy, když jsou **Okraje** nastaveny na **Žádné** v rozšířených vlastnostech tiskárny pro aplikaci Microsoft Excel. Po vygenerování zkušebního šeku povolte úpravy výstupu aplikace Excel a nakonfigurujte rozvržení stránky tak, aby byly všechny okraje nastaveny na **0** (nula). Porovnejte zkušební kopii šeků s vašimi zásobami šeků a upravte nastavení tak, abyste byli spokojeni se zarovnáním.
- Když generujete platby pro nakonfigurovaný bankovní účet v deníku plateb, vytisknou se šeky v zadaném formátu.

Další informace naleznete v tématu [Úprava formátu elektronického výkaznictví](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]