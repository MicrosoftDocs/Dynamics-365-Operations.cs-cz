---
title: Přehled Project Service Automation
description: Toto téma obsahuje informace o řešení integrace Dynamics 365 Project Service Automation do Dynamics 365 Finance.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250546"
---
# <a name="project-service-automation-overview"></a>Přehled Project Service Automation

[!include[banner](../includes/banner.md)]

Řešení integrace Project Service Automation do Finance and Operations používá funkci Integrace dat k synchronizaci dat napříč instancemi Dynamics 365 Finance a Dynamics 365 Project Service Automation prostřednictvím Common Data Service. Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance.

> [!NOTE]
> - Pokud používáte 7.3.0, je nutné nainstalovat KB 4074835. Poté budete schopni integrovat projekty s pevnou cenou.
> - Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, aby byly tyto poplatky zahrnuty ve faktuře projektu.
> - Pokud používáte verzi 8.0, budete moci používat integraci úkolů projektu, kategorie výdajových transakcí, odhady času, odhady výdajů a uzamknutí funkčnosti.
> - Pokud používáte verzi 8.0.1 nebo novější, budete moci synchronizovat skutečné hodnoty.

Než budete moci integrovat Project Service Automation s Finance, musíte nakonfigurovat parametry Project Service Automation. Další informace naleznete v tématu [Parametry integrace Project Service Automation](PSA-parameters.md).

Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:

- Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.
- Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.
- Při správě řádek projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.
- Při správě milníků řádek projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.
- Při správě projektových úkolů v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.
- Při správě kategorií transakcí výdajů ve Finance a jejich přímé synchronizaci z Finance do Project Service Automation.
- Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.
- Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.
- Při vytváření času projektu, výdajů a skutečných hodnot poplatků v Project Service Automation a při vytváření transakcí projektu v deníku integrace Project Service Automation, aby mohly být zaúčtovány ve Finance.

## <a name="data-synchronization"></a>Synchronizace dat

Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance.

> [!NOTE]
> Ne všechny šablony jsou momentálně k dispozici. Šablony budou uvolňovány při jejich dokončení.

[![Parametry integrace Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systémové požadavky pro aplikaci Finance

Pokud chcete používat integrační řešení Project Service Automation do Finance, musíte si nainstalovat Enterprise edition 7.3 s aktualizací Platform 12 nebo novější.

## <a name="system-requirements-for-project-service-automation"></a>Požadavky na systém pro Project Service Automation

Chcete-li použít řešení integrace Project Service Automation do Finance, musíte si nainstalovat následující součásti:

- Dynamics 365 Project Service Automation verze 9.0.0.0 nebo novější
- Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 Sales, verze 1.14.0.0 (v14) nebo pozdější.
- Integrační řešení Project Service Automation do Finance pro Dynamics 365 Project Service Automation verze 1.0.0.0 nebo pozdější

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Nainstalujte řešení integrace Project Service Automation do Finance do své instance Project Service Automation

Stáhněte si řešení integrace Project Service Automation do Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.
