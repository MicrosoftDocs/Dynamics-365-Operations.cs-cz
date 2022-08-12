---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.28. (srpen 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7e17127ff6ef6c52034b8aa5e0c8404772363ca9
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186512"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.28. (srpen 2022)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.28. Tato verze má číslo sestavení 10.0.1264 a je k dispozici podle následujícího plánu:

- **Náhled verze:** květen 2022
- **Obecně dostupné vydání (automatická aktualizace):** červenec 2022
- **Obecně dostupné vydání (automatická aktualizace):** červenec 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a |
|---|---|---|---|
| Zásoby a logistika | [Entity integrace nákladů za doručení pro spediční společnosti třetích stran](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Přehled entit nákladů na doručení](../landed-cost/landed-cost-entities-overview.md) | Ve výchozím nastavení povoleno |
| Plánování | [Plánování materiálových požadavků řízené poptávkou (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Plánování materiálových požadavků řízené poptávkou – přehled](../master-planning/planning-optimization/ddmrp-overview.md) | Správa funkcí:<br>*(Preview) DDMRP pro optimalizaci plánování* |
| Plánování | [Podpora optimalizace plánování řízená prioritou pro příslib na základě dostupné kapacity (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | Již brzy | Správa funkcí:<br>*(Preview) CTP pro optimalizaci plánování* |
| Plánování | [Podpora Optimalizace plánování u skladovatelnosti](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Již brzy | Ve výchozím nastavení povoleno |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Řízení zásob a skladu | Povolit zobrazení pouze nenulového množství na skladě mezipodnikových zásob na skladě | Tato funkce vám umožňuje určit, zda mají být položky s nulovým množstvím na skladě zahrnuty do mezipodnikového seznamu zásob na skladě. Tuto možnost můžete ovládat pomocí nastavení **Nezobrazovat položky s nulovým množstvím na skladě v mezipodnikovém seznamu zásob na skladě**, které tato funkce přidává do stránky **Parametry modulu Řízení zásob a skladu**. |
| Řízení zásob a skladu | (Indie) V případě pravidel převodních cen ignorovat umístění, když je hodnota „Z kódu skladu“ nastavena na „Vše“ | <p>Tato funkce se vztahuje pouze na indické lokalizace. Díky tomu je proces nastavování převodních cen pro položky ve skladových převodech srozumitelnější.</p><p>Převodní ceny nastavíte tak, že každou položku nakonfigurujete pomocí pravidel převodních cen. Jedním ze způsobů, jak provést tuto konfiguraci, je zahrnout řádek pravidla, kde je pole **Kód Ze skladu** nastaveno na *Vše*. Toto nastavení udává, že převodní cena definovaná řádkem by měla platit bez ohledu na sklad, ze kterého je zboží vyskladněno. Když je tato funkce povolena, pravidla převodní ceny, kde je pole **Kód Ze skladu** nastaveno na *Vše*, budou ignorovat **Umístění**. Proto bude pravidlo platit bez ohledu na umístění, které je uvedeno na převodním příkazu. Toto chování je pravděpodobně očekávané, protože umístění je v hierarchii dimenzí úložiště pod skladem.</p><p>Bez této funkce systém použije pravidla tohoto typu pouze v případě, že umístění na převodním příkazu přesně odpovídá umístění nastavenému pro pravidlo. (Pokud je pro pravidlo nastaveno prázdné umístění, systém pravidlo použije pouze na převodní příkazy, které mají pro dané umístění také prázdnou hodnotu.)</p> |
| Řízení zásob a skladu | Vyčištění dat výkazu zásob na skladě | Tato funkce poskytuje způsob, jak vyčistit data použitá k vytváření sestav *Úložiště sestavy zásob na skladě*. |
| Řízení výroby | Přiřaďte projektové aktivity pro řádky servisní smlouvy a servisní objednávky | Tato funkce přidá pole s názvem **Aktivita projektu** do řádků servisní smlouvy a servisní objednávky, abyste pro ně mohli nastavit aktivitu projektu. Tato funkce pomůže zabránit chybám blokování při zaúčtování deníků projektu správy služeb, které vyžadují nastavení aktivity projektu.  |
| Řízení skladu | Služba ručního výdeje řádku převodu pro správce nebo podobné důvěryhodné uživatele | Tato funkce umožňuje správcům ručně vybírat transakce zásob, které souvisejí s převodními řádky. Tyto řádky zahrnují řádky, které již byly uvolněny do skladu. Správci by měli tento výběr provádět pouze ve výjimečných případech, například když je systém v poškozeném stavu. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující články nápovědy. Tento článek nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozích částech. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nové nebo aktualizované články |
|---|---|
| Správa nákladů | [Pevná cena příjmu](../cost-management/fixed-receipt-price.md) |
| Správa nákladů | [Často kladené otázky o ceně zásob](../cost-management/inventory-costing-faq.md) |
| Správa nákladů | [Princip účtování na účet poplatků](../cost-management/post-to-charge-account-accounting-principle.md) |
| Řízení zásob | [Podrobnosti transakce zásob](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.28 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.28 finančních a provozních aplikací (červen 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.28, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022](/dynamics365-release-plan/2022wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Článek [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

