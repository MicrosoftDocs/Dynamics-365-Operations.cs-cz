---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.30. (listopad 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2983c113487934fd0751efcef9129e1f28d8dce8
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714791"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.30. (listopad 2022)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.30. Tato verze má číslo sestavení 10.0.1362 a je k dispozici podle následujícího plánu:

- **Verze Preview:** září 2022
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2022
- **Obecně dostupné vydání (automatická aktualizace):** Listopad 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Výroba | [Monitorování zařízení pomocí funkce Sensor Data Intelligence](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Úvodní stránka Sensor Data Intelligence](../sensor-data-intelligence/sdi-home-page.md) | Správa funkcí:<br>*(Preview) Sensor Data Intelligence* |
| Řízení skladu | [Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Konfigurace náhradního procesu pro kroky v položkách nabídky mobilního zařízení](../warehousing/warehouse-app-detours.md) | Správa funkcí:<br>*Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Řízení výroby | Informace o množství na skladě na stránce výrobních zakázek k uvolnění | Přidá sloupec pro množství zásob na skladě pro řádkovou položku v sekci řádků na stránce **Výrobní zakázky k uvolnění**. |
| Správa přepravy | Přiřazení dodávek k souvisejícím segmentům trasy | Tato funkce umožňuje systému přesněji rozdělovat náklady na přepravu zásilek, včetně nákladů s více zásilkami doručovanými do různých destinací segmentů po jedné trase. Každou zásilku přiřadí k nejvhodnějšímu segmentu trasy na základě cílové adresy zásilky a segmentu. Tato funkce pak vypočítá náklady na přepravu každé zásilky jako podíl celkových nákladů na přepravu nákladu na základě relativní hmotnosti, objemu, množství a ujeté vzdálenosti zásilky. Tato funkce se vztahuje pouze na zásilky spravované pomocí modulu Správa přepravy (TMS). |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.30 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.30 aplikací Finance a Operace (listopad 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.30, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022](/dynamics365-release-plan/2022wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Článek [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
