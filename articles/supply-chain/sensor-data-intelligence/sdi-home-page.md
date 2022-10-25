---
title: Úvodní stránka Sensor Data Intelligence
description: Tento článek podává přehled o Sensor Data Intelligence. Organizace mohou tuto funkci využít k řízení obchodních procesů v Microsoft Dynamics 365 Supply Chain Management na základě signálů internetu věcí (IoT) ze strojů a zařízení ve výrobě.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689850"
---
# <a name="sensor-data-intelligence-home-page"></a>Úvodní stránka Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensor Data Intelligence pro Microsoft Dynamics 365 Supply Chain Management umožňuje organizacím řídit obchodní procesy v Supply Chain Management na základě signálů internetu věcí (IoT) ze strojů a zařízení ve výrobě. Je to aktualizovaná, přejmenovaná verze funkce *IoT Intelligence*, která byla dříve dostupná pro Supply Chain Management.

Sensor Data Intelligence umožňuje provádět následující činnosti:

- Shromažďováním údajů o strojích a zařízeních aktualizovat hodnoty počítadel objektu údržby v Supply Chain Management a řídit prediktivní údržbu.
- Nastavit řešení pomocí jednoduchého průvodce onboardingem namísto ruční instalace a konfigurace součástí v Microsoft Dynamics Lifecycle Services (LCS).
- Nasazovat komponenty ve vlastním předplatném, abyste měli větší flexibilitu při správě komponent Azure.
- Konfigurovat, škálovat a rozšiřovat řešení jako obchodní logiku, která běží na komponentách Azure. Tyto komponenty jsou nyní spravovány ve vašem vlastním předplatném. Proto je můžete přizpůsobit podle potřeby tak, aby vyhovovaly vašim jedinečným obchodním potřebám.

## <a name="business-scenarios"></a>Obchodní scénáře

Sensor Data Intelligence umožňuje několik typů funkcí, z nichž každá je reprezentována specifickým *scénářem* v systému. Každý scénář poskytuje specializovanou sadu konfiguračních možností v systému, jak je podrobně uvedeno v následující tabulce.

| Scénář | Popis |
|---|---|
| [Výpadek prostředku](sdi-scenario-asset-downtime.md) | Přesně sledujte efektivitu strojního vybavení pomocí dat ze senzorů ke sledování prostojů stroje. |
| [Údržba majetku](sdi-scenario-asset-maintenance.md) | Minimalizujte náklady na údržbu a prodlužte životnost zařízení zlepšením plánů údržby založených na snímaných hodnotách kritických kontrolních bodů pro strojní zařízení. |
| [Stav zařízení](sdi-scenario-equipment-downtime.md) | Zajistěte efektivitu provozu pomocí odečtů senzorů k upozorňování plánovačů na výpadky stroje a poskytování možností pro zmírnění potenciálních zpoždění. |
| [Kvalita produktu](sdi-scenario-product-quality.md) | Zajistěte kvalitu šarží produktů porovnáním hodnot senzorů se skutečnými vlastnostmi každé šarže produktu, jako je vlhkost, teplota nebo vlastní metriky kvality. Systém upozorní uživatele, když nastanou odchylky. |
| [Zpoždění výroby](sdi-scenario-production-delays.md) | Použijte odečet senzorů k porovnání skutečné doby cyklu s plánovanou dobou cyklu a upozorněte nadřízené, když výroba není podle plánu. Nadřízení pak mohou podle potřeby zasahovat, aby byla zajištěna maximální efektivita provozu. |

## <a name="architecture"></a>Architektura

Následující architektonický diagram poskytuje přehled řešení a jeho součástí.

![Architektonický diagram Sensor Data Intelligence.](media/sdi-architecture.png "Architektonický diagram Sensor Data Intelligence")
