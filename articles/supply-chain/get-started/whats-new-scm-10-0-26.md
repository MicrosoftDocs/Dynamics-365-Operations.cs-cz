---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.26. (květen 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: d47f3f377a7de87b9c24a18e4542e5a48235d270
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954473"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.26. (květen 2022)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.26. Tato verze má číslo sestavení 10.0.1192 a je k dispozici následujícím způsobem:

- **Náhled verze:** březen 2022
- **Obecně dostupné vydání (vlastní aktualizace):** duben 2022
- **Obecně dostupné vydání (automatická aktualizace):** květen 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Zásoby a logistika | [Přímý dotaz k viditelnosti zásob na podporu položek pokročilou správu skladu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Podpora Inventory Visibility pro položky WHS](../inventory/inventory-visibility-whs-support.md) | Správa funkcí:<br>*Povolte skladové položky ve viditelnosti zásob* |
| Zásoby a logistika | [Dostupné jako příslib pro doplněk viditelnosti skladu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](../inventory/inventory-visibility-available-to-promise.md) | Aktivováno konfigurací služeb |
| Výroba | [Položky skutečné hmotnosti pro rozhraní ke spuštění výrobního provozu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md) | Správa funkcí:<br>*(Preview) Sestava položek skutečné hmotnosti z rozhraní provádění výrobního provozu* |
| Výroba | Karta Moje úlohy v rozhraní pro provádění výrobního provozu <!-- KFM: Add link to release plan when available --> | [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md) | Správa funkcí:<br>*Karta Moje úlohy v rozhraní pro provádění výrobního provozu* |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Zásobování a zdroje | Účtujte registrovaná množství produktů na skladě a zbytky neskladových produktů pro účtenky a faktury dodavatele | Tato funkce mění způsob zaúčtování množství neskladovaných produktů (jako jsou služby) při zpracování faktur dodavatele a příchozích zásilek oproti nákupním objednávkám. Tato funkce upravuje chování množství *Registrované množství a služby* pro zaúčtování příjemek a faktur dodavatelů změnou tak, aby odpovídala chování možnosti *Registrované množství a neskladované produkty* již poskytnuté při účtování množství na prodejních balicích listech.<br><br>Když zaúčtujete příjemku produktu nebo fakturu dodavatele pomocí možnosti množství *Registrované množství a služby*, systém zaúčtuje evidované množství naskladněných produktů a zaúčtuje zbývající množství neskladovaných produktů (včetně služeb i neslužeb). Bez této funkce systém stále účtuje registrované množství naskladněných produktů (včetně služeb nakonfigurovaných jako skladové položky), ale vždy účtuje celé objednané množství nenaskladněných servisních produktů (a ignoruje neskladované produkty, které nejsou typu *Služba*). |
| Zásobování a zdroje | Synchronizovat sledovací dimenze na řádcích mezipodnikových prodejních a nákupních objednávek | Tato funkce vám umožňuje řídit, zda jsou dimenze sledování sériového čísla a čísla šarže synchronizovány napříč mezipodnikovými prodejními a nákupními řádky. Do obou přidává nová nastavení ke kartám **Zásady nákupní objednávky** i **Zásady prodejní objednávky** stránky nastavení **Mezipodnikové** pro zákazníky a prodejce. Pro srozumitelnost také aktualizuje názvy několika souvisejících blízkých nastavení.<br><br>Pokud používáte pokročilé řízení skladu (WMS), tato funkce bude synchronizovat čísla dávky a série pouze tehdy, když jsou tyto dimenze nad umístěním v hierarchii rezervace cílového umístění. |
| Správa informací o produktech | Vyčistit hodnoty atributů produktu | Tato funkce přidává pravidelnou úlohu nazvanou **Vyčistit hodnoty atributů produktu**, která vyčistí záznamy hodnot atributů produktu, které již nejsou přidruženy k žádnému produktu prostřednictvím kategorie produktu. |
| Řízení zásob a skladu | (Rusko) Zabránit nesrovnalostem při vydávání GTD pro nákupní objednávky, které obsahují položky s povoleným WMS | Tato funkce je dostupná pouze pro ruskou lokalizaci. Zabraňuje nesrovnalostem, ke kterým dochází při vydávání ruských čísel celních prohlášení (GTD) pro importní nákupní objednávky, které obsahují položky s povoleným pokročilým skladem (WMS). Proces vystavení GTD mění některé hodnoty dimenzí zásob v souvisejících transakcích zásob pro faktury zahrnuté ve vlastním deníku, což vede k nesrovnalostem mezi pracovními záznamy pro nákupní objednávku a transakcemi zásob pro nákup. Když je tato funkce povolena, proces vydávání GTD generuje seřizovací práce, které tyto nesrovnalosti eliminují. |
| Řízení skladu | Vylepšený analyzátor pro čárové kódy GS1 | Tato funkce přidává vylepšený analyzátor pro data symbolů GS1. Nový parser implementuje algoritmus GS1 General Specification pro analýzu symbolů GS1 a poskytuje silnější validaci dat. Více informací získáte v části [Skenování čárových kódů GS1](../warehousing/gs1-barcodes.md). |
| Řízení skladu | Nové stránky pracovní plochy plánování vytížení | Přidává dvě nové stránky pracovní plochy pro plánování vytížení: **Pracovní plocha pro plánování příchozího vytížení** a **Pracovní plocha pro plánování odchozího vytížení**. |
| Řízení skladu | Aplikace řízení skladu - prázdné GTD | Tato funkce je dostupná pouze pro ruskou lokalizaci. Umožňuje pracovníkům, kteří používají mobilní aplikaci Warehouse Management, nechat v případě potřeby čísla ruských celních prohlášení (GTD) prázdná. Pokud je dimenze sledování GTD nastavena tak, aby umožňovala prázdné hodnoty, systém bude přijímat prázdné hodnoty pro GTD pro operace zásob, pokud je k dispozici inventář na skladě. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující články nápovědy. Tento článek nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozích částech. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nové nebo aktualizované články |
|---|---|
| Správa nákladů | Ke každému z následujících článků byly přidány aktualizované příklady a diagramy:<ul><li>[Metoda FIFO s fyzickou hodnotou a označením](../cost-management/fifo-physical-value-marking.md)</li><li>[Metoda LIFO s fyzickou hodnotou a označením](../cost-management/lifo-physical-value-marking.md)</li><li>[Datum LIFO s fyzickou hodnotou a označením](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Průběžná průměrná nákladová cena](../cost-management/running-average-cost-price.md)</li><li>[Vážený průměr s fyzickou hodnotou a označením](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.26 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.26 finančních a provozních aplikací (květen 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.26, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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
