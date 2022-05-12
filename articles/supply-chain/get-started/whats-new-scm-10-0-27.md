---
title: Náhled Dynamics 365 Supply Chain Management 10.0.27 (červenec 2022)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e8ec20c361f76a6012a7c8e1f03296007f5a05aa
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645342"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Náhled Dynamics 365 Supply Chain Management 10.0.27 (červenec 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.27. Tato verze má číslo sestavení 10.0.1227 a je k dispozici podle následujícího plánu:

- **Verze Preview:** duben 2022
- **Obecně dostupné vydání (vlastní aktualizace):** červen 2022
- **Obecně dostupné vydání (automatická aktualizace):** červenec 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tohle téma můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Zásoby a logistika | [Přidělení skladových zásob jako příslib pro doplněk viditelnosti skladu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | Již brzy | Ve výchozím nastavení povoleno |
| Výroba | Zobrazení Můj den pro rozhraní pro provádění výrobního provozu | [Jak pracovníci používají rozhraní pro provádění výrobních operací ve výrobní hale](../production-control/production-floor-execution-use.md) a [Zobrazení zůstatků dovolené v rozhraní pro provádění ve výrobní hale](../production-control/production-floor-execution-payroll-stats.md) | Správa funkcí:<br>*Zobrazení Můj den pro rozhraní pro provádění výrobního provozu* |
| Plánování | [Podpora Optimalizace plánování u subdodávek](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Správa subdodavatelské práce při výrobě](../production-control/manage-subcontract-work-production.md) | Ve výchozím nastavení povoleno |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Hlavní plánování | Při vytváření plánovaného převodního příkazu vezměte v úvahu dobu realizace zásob | Když se vytvoří plánovaný převodní příkaz, tato funkce způsobí, že systém vezme v úvahu dobu realizace zásob zadanou ve výchozím nastavení objednávky položky při výpočtu data přijetí plánovaného převodního příkazu pro nastavení řízení data dodání jako *Žádné* nebo typ *prodeje*. Je-li specifikována doba realizace převodu, její hodnota bude převzata pro výpočet data přijetí a dny přepravy nebudou brány v úvahu. Pokud je uvedena doba realizace přenosu potenciálního zákazníka, použije se její hodnota pro výpočet data přijetí a dny přepravy se neberou v úvahu. |
| Zásobování a zdroje | Výchozí informace o dani smluv zprostředkovatelů na řádcích faktury dodavatele | Tato funkce zavádí logiku pro nastavení výchozích hodnot pro pole **DPH** a **Daň z prodeje zboží** na řádcích faktury dodavatele smlouvy zprostředkovatele. Tato logika se použije pouze v případě, že typ poplatku na řádku zprostředkovatelské smlouvy je hlavní kniha/hlavní kniha. Skupina daně z prodeje položky převezme svou výchozí hodnotu buď z kategorie zprostředkovatelských zakázek (pokud je nastavena), nebo z typu poplatku. Skupina prodejní daně bude používat výchozí hodnotu z účtu dodavatele. |
| Zásobování a zdroje | Omezit počet řádků nákupní objednávky na dávkovou úlohu | Tato funkce vám pomáhá optimalizovat výkon systému, když jsou zaúčtovány potvrzení a účtenky produktu. Přidá nové nastavení s názvem **Řádky na úkol** na kartu **Dodání** stránky **Parametry nákupu a zajištění zdrojů**. Toto nové nastavení vám umožňuje omezit počet řádků nákupní objednávky, které každá dávková úloha zpracovává. Proto může pomoci zabránit velkým dávkovým úlohám ve zpomalení systému. |
| Správa informací o produktech | Vyplnit hodnoty atributů produktu | Tato funkce přidává pravidelnou úlohu s názvem *Naplnit hodnoty atributů produktu*. Tato nová pravidelná úloha vytváří chybějící záznamy hodnot atributů produktu pro atributy přidružené k produktům prostřednictvím kategorie produktu. |
| Řízení výroby | Další konfigurace v rozhraní pro provádění výrobního provozu | <p>Tato funkce přidává následující možnosti na stránku **Konfigurace provádění výrobního provozu**:</p><ul><li>**Automatické otevření dialogového okna spuštění** – Pokud je tato možnost nastavena na Ano, když pracovníci použijí vyhledávací panel k vyhledání úlohy, automaticky se otevře dialogové okno **Zahájení úlohy**.</li><li>**Automatické otevření dialogového okna pokroku sestavy** – Pokud je tato možnost nastavena na Ano, když pracovníci použijí vyhledávací panel k vyhledání úlohy, automaticky se otevře dialogové okno **Pokrok sestavy** pro úlohu.</li><li>**Výchozí zbývající množství v dialogovém okně průběhu sestavy** – Když je tato možnost povolena, dialogové okno **Hlásit pokrok** zobrazuje zbývající množství pro hlášení o výrobní úloze.</li></ul><p>Další informace viz [Konfigurace rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md).</p> |
| Řízení výroby | Produkční týmy v rozhraní pro provádění výrobního provozu | <p>Když je ke stejné výrobní úloze přiděleno více pracovníků, mohou nyní nominovat jednoho pracovníka jako pilota. Zbývající pracovníci se pak automaticky stanou asistenty tohoto pilota. U výsledného týmu musí pouze pilot registrovat stav úlohy, zatímco časové záznamy se vztahují na všechny členy týmu. Tato funkce také podporuje scénář s názvem *pomocný zdroj*. V tomto scénáři se pracovník může zaregistrovat jako asistent jiného pracovníka, který se pak stane pilotem pro nově vytvořenou skupinu.</p><p>Další informace viz [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md).</p> |
| Řízení výroby | Vykazování položek plánování v rozhraní pro provádění výrobního provozu | Tato funkce zjednodušuje proces hlášení o dávkových objednávkách pro plánování položek v rozhraní realizace výrobního podlaží. Když je vytvořena dávková objednávka pro produkt, který má typ výroby *Položka plánování* hlášení jako dokončené lze provést pouze u vedlejších produktů a vedlejších produktů pro danou dávkovou objednávku. Dávkové objednávky pro položky plánování se obvykle používají k podpoře procesů demontáže, kdy je produkt ze surového materiálu rozebrán na několik různých produktů. Když pracovník nahlásí dávkovou objednávku pro položku plánování jako dokončenou, dialogové okno **Hlásit pokrok** nyní zobrazí pouze vedlejší produkty. Dříve také zobrazovalo položku plánování a toto chování mohlo zmást pracovníky. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Tato témata nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozích částech. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Správa nákladů | [Denní vážený průměr se zahrnutím fyzické hodnoty a označením](../cost-management/weighted-average-date.md) |
| Distribuovaná hybridní topologie | [Vyzkoušejte jednotky škálování v distribuované hybridní topologii](../cloud-edge/cloud-edge-try-out.md) |
| Duální zápis | [Synchronizace na požádání s cenovým modulem Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Řízení skladu | [Uvolnění do skladu](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.27 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.27 finančních a provozních aplikací (červen 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.27, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022](/dynamics365-release-plan/2022wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
