---
title: Modul informací o vyzvednutí
description: Tohle téma se zabývá modulem informací o vyzvednutí a popisuje, jak jej přidat na stránky pokladny v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9428eda880d534c700646b52310c6b8befdebaf2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353797"
---
# <a name="pickup-information-module"></a>Modul informací o vyzvednutí

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem informací o vyzvednutí a popisuje, jak jej přidat na stránky pokladny v řešení Microsoft Dynamics 365 Commerce.

Modul informací o vyzvednutí lze použít v modulu pokladny k zobrazení informací o vyzvednutí objednávky. Zákazníci si mohou prohlédnout dostupná data vyzvednutí a časové úseky a poté vybrat vhodný čas pro vyzvednutí objednávky. Například si zákazník může vybrat vyzvednutí objednávky v 15:00 dne 21. března v obchodě v San Francisku.

Časové úseky vyzvednutí pro příslušné obchody musí být nakonfigurovány v centrále Commerce. Další informace viz [Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem](dev-itpro/pickup-timeslots.md).

Pokud je na stránce pokladny vytvořen modul s informacemi o vyzvednutí, ale pro obchod, který je vybrán pro vyzvednutí, nejsou definovány žádné časové úseky, modul zobrazí informace, ale uživatel nebude moci vybrat žádné časové úseky. Časové úseky jsou volitelné a nejsou nutné k zadání objednávky.

Pokud je pro vyzvednutí vybráno více položek ve více obchodech, modul s informacemi o vyzvednutí umožní uživateli vybrat časový úsek pro každý obchod za předpokladu, že jsou pro něj dostupné.

> [!NOTE]
> Podpora časových úseků a modul informací o vyzvednutí v pokladně je k dispozici v Dynamics 365 Commerce verze 10.0.15 a novější.

Následující obrázek ukazuje příklad výběru časového úseku prostřednictvím modulu s informacemi o vyzvednutí na stránce pokladny.

![Příklad modulu s informacemi o vyzvednutí na stránce pokladny.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

- **Nadpis** – Zadejte nadpis modulu.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Zobrazení informací o časovém úseku po zadání objednávky

Po zadání objednávky lze informace o vybraném časovém úseku zobrazit v [modulu potvrzení objednávky](order-confirmation-module.md) a [modul podrobností objednávky](account-management.md#order-details-page). Oba tyto moduly mají vlastnost **Zobrazit informace o časovém úseku**. Aby mohly během procesu objednávky zobrazit vybraný časový úsek, musí být tato vlastnost nastavena na **Pravda**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Přidání modulu s informacemi o vyzvednutí na pokladně na stránce

Pokyny k přidání modulu s informacemi o vyzvednutí na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).

Následující ilustrace ukazuje příklad stránky pokladny elektronického obchodu, která obsahuje časové úseky pro vyzvednutí řádkových položek.

![Příklad stránky pokladny elektronického obchodu, která obsahuje časové úseky pro vyzvednutí řádkových položek.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Další prostředky

[Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem](dev-itpro/pickup-timeslots.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul podrobností objednávky](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]