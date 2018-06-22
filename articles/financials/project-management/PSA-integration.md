---
title: Project Service Automation
description: "Toto řešení používá funkci integrace dat k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations a Dynamics 365 for Project Service Automation prostřednictvím služby Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations a Dynamics 365 for Project Service Automation prostřednictvím služby Common Data Service (CDS). Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance and Operations.

> [!NOTE] 
> Pokud používáte aplikaci Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, musíte si nainstalovat KB 4074835. To vám poskytne integrovat projekty s pevnou cenou.
>
> Pokud používáte Dynamics 365 for Finance and Operations verzi 8.0, budete moci používat integraci úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí.
>
> Pokud používáte Dynamics 365 for Finance and Operations verze 8.0.1, bude možné synchronizovat skutečné hodnoty.
>
> Pokud používáte Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.

Než budete moci integrovat Project Service Automation s Finance and Operations, musíte nakonfigurovat parametry Project Service Automation. Další informace naleznete v tématu parametry integrace Project Service Automation.

Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:

- Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě řádků projektových smluv v Project Service Automation a jeijch přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě milníků řádků projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě projektových úloh v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě kategorií transakcí výdajů v Finance and Operations a jejich přímé synchronizaci z Finance and Operations do Project Service Automation.
- Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.

## <a name="data-synchronization"></a>Synchronizace dat
Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance and Operations.

> [!NOTE]
> Ne všechny šablony jsou momentálně k dispozici. Šablony budou uvolňovány při jejich dokončení.

[![Integrace Project Service Automation s aplikací Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations

Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 s aktualizací platform update 12 nebo novější.

## <a name="system-requirements-for-project-service-automation"></a>Požadavky na systém pro Project Service Automation

Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat následující součásti:

- Microsoft Dynamics 365 for Project Service Automation , verze 9.0.0.0 nebo novější.
- Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.
- Řešení Project Service Automation do Operations pro Dynamics 365 for Project Service Automation verze 1.0.0.0 nebo novější.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Nainstalujte řešení integrace Project Service Automation do Finance and Operations do své instance Project Service Automation



