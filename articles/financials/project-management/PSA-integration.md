---
title: Přehled Project Service Automation
description: Toto téma poskytuje informace o řešení integrace Project Service Automation do Finance and Operations. Toto integrační řešení používá funkci integrace dat a synchronizaci dat mezi instancemi Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation prostřednictvím Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865621"
---
# <a name="project-service-automation-overview"></a>Přehled Project Service Automation

[!include[banner](../includes/banner.md)]

Integrační řešení Project Service Automation to Finance and Operations používá funkci Integrace dat k synchronizaci dat napříč instancemi Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation prostřednictvím Common Data Service. Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance and Operations.

> [!NOTE]
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.
> - Pokud používáte Finance and Operations 7.3.0, je nutné nainstalovat KB 4074835. Poté budete schopni integrovat projekty s pevnou cenou.
> - Pokud používáte Finance and Operations 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, aby byly tyto poplatky zahrnuty ve faktuře projektu.
> - Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0, budete moci používat integraci úkolů projektu, kategorie výdajových transakcí, odhady času, odhady výdajů a uzamknutí funkčnosti.
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations verze 8.0.1, nebo novější, budete moci synchronizovat skutečné hodnoty.

Než budete moci integrovat Project Service Automation s Finance and Operations, musíte nakonfigurovat parametry Project Service Automation. Další informace naleznete v tématu [Parametry integrace Project Service Automation](PSA-parameters.md).

Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:

- Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě řádků projektových smluv v Project Service Automation a jeijch přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě milníků řádků projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě projektových úloh v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při správě kategorií transakcí výdajů v Finance and Operations a jejich přímé synchronizaci z Finance and Operations do Project Service Automation.
- Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.
- Při vytváření času projektu, výdajů a skutečných hodnot poplatků v Project Service Automation a při vytváření transakcí projektu v deníku integrace Project Service Automation, aby mohly být zaúčtovány v Finance and Operations.

## <a name="data-synchronization"></a>Synchronizace dat

Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance and Operations.

> [!NOTE]
> Ne všechny šablony jsou momentálně k dispozici. Šablony budou uvolňovány při jejich dokončení.

[![Integrace Project Service Automation s aplikací Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations

Pokud chcete používat integrační řešení Project Service Automation to Finance and Operations, musíte si nainstalovat Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 s aktualizací platformy 12 nebo novější.

## <a name="system-requirements-for-project-service-automation"></a>Požadavky na systém pro Project Service Automation

Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat následující součásti:

- Microsoft Dynamics 365 for Project Service Automation verze 9.0.0.0 nebo novější
- Řešení zpeněžení potenciálního zákazníka pro Microsoft Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.
- Integrační řešení Project Service Automation to Finance and Operations pro Microsoft Dynamics 365 for Project Service Automation verze 1.0.0.0 nebo pozdější

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Nainstalujte řešení integrace Project Service Automation do Finance and Operations do své instance Project Service Automation

Stáhněte si řešení integrace Project Service Automation do Finance and Operations z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.
