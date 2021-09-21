---
title: Verze Preview Dynamics 365 Supply Chain Management 10.0.22 (listopad 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6fc4b9d0a0f5319c8a75e7d687ee82ea81497844
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471853"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Verze Preview Dynamics 365 Supply Chain Management 10.0.22 (listopad 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.22. Tato verze má číslo sestavení 10.0.995 a je k dispozici následujícím způsobem:

- **Verze Preview:** září 2021
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2021
- **Obecně dostupné vydání (automatická aktualizace):** Listopad 2021

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci. Chcete -li zjistit, jak zapnout funkci, podívejte se na sloupec *Povoleno uživatelem*. Další informace o tom, jak používat správu funkcí, naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tohle téma můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Plánování | [Podpora optimalizace plánování pro přidělování zdrojů na základě schopností](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Plánování s nekonečnou kapacitou](../master-planning/planning-optimization/infinite-capacity-planning.md) | Správa funkce: (*Plánování s nekonečnou kapacitou pro Optimalizaci plánování*) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak). Pokud chcete použít některou z těchto funkcí, musíte ji výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Oblast funkce | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Správa nákladů | Vytvoření souvisejících poukazů pro standardní zaokrouhlování nákladů | <p>Když je provedeno finanční zaúčtování zásob (například faktura prodejní objednávky nebo transakce zásob), tato funkce způsobí, že systém vytvoří samostatný doklad pro jakékoli související přecenění zaokrouhlování standardních nákladů a připojí jej k dokladu o finančním účtování jako související doklad.</p><p>Bez této funkce systém zaznamenává standardní přecenění zaokrouhlení nákladů na stejné zaúčtování poukázky. Toto chování může někdy způsobit konfliktní informace o datu, protože přecenění používají relaci nebo systémové datum, zatímco finanční účtování používá datum účtování.</p> |
| Distribuovaná hybridní topologie | *(Není vyžadována žádná správa funkcí.)* | <p>Tato verze rozšiřuje možnosti plánování odchozího zatížení úlohy správy skladu pro cloudové a hraniční škálovací jednotky.</p><p>Další informace naleznete v části [Pracovní zatížení pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Správa technických změn | Generování varianty pro technické produkty | <p>Tato funkce vám umožňuje generovat několik variant pro technický produkt na základě jeho barvy, velikosti, stylu nebo rozměrů konfigurace.</p><p>Další informace viz [Generování variant pro strojírenské výrobky](../engineering-change-management/engineering-variants.md).</p> |
| Řízení zásob a skladu | Integrace viditelnosti zásob s posunem rezervace | <p>Tuto funkci lze povolit až po povolení funkce *Integrace viditelnosti zásob*. Poskytuje funkce pro kompenzaci rezervací, které jsou provedeny na viditelnosti zásob.</p><p>Další informace viz [Rezervace ve Viditelnosti zásob](../inventory/inventory-visibility-reservations.md).</p> |
| Prodej a marketing | Omezit počet prodejních objednávek, které lze vybrat k zaúčtování | <p>Tato funkce je povolena automaticky. Přidává pole s názvem **Max. počet prodejních objednávek k zaúčtování** na stránku **Parametry pohledávek**. Toto pole vám umožňuje definovat maximální počet prodejních objednávek, které lze vybrat při zaúčtování potvrzení, výdejek, dodacích listů a faktur ze stránky seznamu prodejních objednávek. Výchozí hodnota je *100*.</p><p>Tato funkce pomáhá zlepšit výkon stránky seznamu prodejních objednávek, když je vybrán značný počet prodejních objednávek. Nemá to žádný vliv na počet prodejních objednávek, které lze zpracovat periodickým úkolem.</p> |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Tato témata nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozí části. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Správa technických změn | [Přehled správy technických změn](../engineering-change-management/product-engineering-overview.md) nyní uvádí všechny související volitelné funkce dostupné ve správě funkcí |
| Hlavní plánování | [Nastavení prognózy poptávky](../master-planning/demand-forecasting-setup.md) |
| Hlavní plánování | [Čisté požadavky a informace o doložení u optimalizace plánování](../master-planning/planning-optimization/net-requirements.md) |
| Řízení skladu | [Uvolnit do skladu](../warehousing/release-to-warehouse-process.md) poskytuje podrobný přehled procesu úplného uvolnění do skladu |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.22 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.22 aplikací Finance and Operations (listopad 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.22, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021](/dynamics365-release-plan/2021wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
