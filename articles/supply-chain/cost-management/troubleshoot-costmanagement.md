---
title: Řešení potíží se správou nákladů
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se správou nákladů.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b8c527e578fee6abfeeade99fba8070365c020bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983843"
---
# <a name="troubleshoot-cost-management"></a>Řešení potíží se správou nákladů

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se správou nákladů.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funkční mezery mezi sestavami o hodnotě/stárnutí zásob a jejich verzemi úložiště

Funkce [Uložení sestavy stáří zásob](inventory-aging-report-storage.md) a [Sestava úložiště hodnot zásob](inventory-value-report-storage.md) umožňují aplikaci Supply Chain Management zobrazit velké objemy transakcí zásob. V každém případě se výsledky sestavy ukládají k procházení a exportu, na rozdíl od verzí těchto sestav bez úložiště. Některé funkce, které existují ve verzích těchto sestav bez úložiště, však ve verzích úložiště neexistují. Následující pododdíly shrnují rozdíly a poskytují alternativní řešení.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Sestavy úložiště nezahrnují mezisoučty, i když jsou povoleny v rozložení sestavy

Mezisoučty mohou způsobit problémy při exportu výsledku, zejména pokud uživatelé změní sekvenci záznamů.

Chcete-li zkontrolovat mezisoučty, můžete exportovat výsledek do Microsoft Excel. Alternativně, pokud chcete zkontrolovat mezisoučty v rámci Supply Chain Management, použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a povolte funkce *Nový ovládací prvek mřížky* a *(Preview) Seskupení do mřížek*, které poskytují mnohem flexibilnější způsob, jak zobrazit mezisoučet pro každou skupinu podle sloupce. Další informace naleznete v části [Schopnosti mřížky](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Sestava úložiště hodnot zásob nepodporuje informace o účtu hlavní knihy

Můžete spustit předvahu, abyste získali zůstatek na účtech zásob a porovnali jej se sestavou **Úložiště hodnot zásob**.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Varování nebo chyby se zobrazují při změně stavu období hlavní knihy bez uzávěrky skladu.

Společnost Microsoft zavedla následující ověření, aby zabránila problémům způsobeným nesprávným procesem na konci období kolem výpočtu nákladů. Pokud narazíte na některou z následujících chybových zpráv, podívejte se na [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) ohledně informací o řešení těchto problémů.

- Chystáte se provést přepočet s datem %1 (10-02-2019). Poslední registrovaný přepočet byl proveden v předchozím období s datem %2 (20-01-2019). Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 (31-01-2019) nebylo zaregistrováno. Nezapomeňte provést uzávěrku skladu k datu konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

- Chystáte se změnit stav období hlavní knihy %1 na %2. Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 nebylo zaregistrováno. Proveďte prosím uzávěrku skladu k datu konce odpovídajícího období %3 před změnou stavu. Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno. Hlášeno z právnické osoby %4. Prozatím je to informační, ale v budoucnu budete muset provést takovou akci.

- Účetní struktura %1 byla změněna. Jeden nebo více hlavních účtů %2 již neexistuje. Tyto hlavní účty jsou vyžadovány %3 s datem %4. Přidejte tyto hlavní účty do účetní struktury %1, než budete moci obnovit úlohu %3. Prozatím je to informační, ale v budoucnu budete muset provést takovou akci.

- Chystáte se provést uzávěrku skladu s datem %1 (31-01-2019). Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %2 (31-01-2019) nebylo zaregistrováno. Nezapomeňte spustit výpočet zpětného účtování nákladů s datem konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

- Chystáte se provést výpočet zpětného účtování nákladů s datem %1 (28-02-2019). Poslední registrovaný výpočet zpětného účtování nákladů byl proveden v předchozím období s datem %2 (31-01-2019). Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 (31-01-2019) nebylo zaregistrováno.
Nezapomeňte provést uzávěrku skladu k datu konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud nebude uzávěrka skladu provedena.

## <a name="inventory-aging-report-discrepancies"></a>Nesrovnalosti sestavy stáří zásob

**Sestava stáří zásob** zobrazuje různé hodnoty při zobrazení v různých dimenzích úložiště (například jako pracoviště nebo sklad). Další informace o logice vykazování najdete v tématu [Příklady a logika sestav stáří zásob](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Konflikt aktualizace nastane, když metoda ocenění zásob je buď Standardní cena nebo Klouzavý průměr

Když paralelně zaúčtujete dokumenty, jako jsou deníky zásob, faktury za nákupní objednávky nebo faktury od prodejní objednávky, kvůli škálovatelnosti a výkonu, může se zobrazit chybová zpráva o konfliktu aktualizací a některé dokumenty se nemusí zaúčtovat. Tento problém nastane, když metoda ocenění zásob je buď *Standardní cena* nebo *Klouzavý průměr*. Obě tyto metody jsou metody stálého výpočtu nákladů. Jinými slovy, konečná cena je stanovena v době zveřejnění.

Pokud používáte metodu *Klouzavý průměr*, chybová zpráva se podobá tomuto příkladu:

> Po výpočtu proporcionálních výdajů se neočekává hodnota zásob xx.xx

Pokud používáte metodu *Standardní náklady*, chybová zpráva se podobá tomuto příkladu:

> Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci. Hodnota = xx.xx, množství = rr.rr, standardní cena = zz.zz

Dokud společnost Microsoft nevydá řešení k vyřešení problému, zvažte použití následujících řešení, která vám pomohou těmto chybám zabránit nebo je snížit:

- Znovu odešlete chybné dokumenty.
- Vytvářejte dokumenty, které mají méně řádků.
- Ve standardní ceně se vyhněte desítkovým hodnotám. Zkuste definovat standardní cenu tak, aby pole **Cenové množství** bylo nastaveno na *1*. Pokud musíte zadat hodnotu **Cenové množství**, která je větší než *1*, zkuste minimalizovat počet desetinných míst v jednotkové standardní ceně. (V ideálním případě by měla být méně než dvě desetinná místa.) Například se vyhněte definování standardního nastavení nákladů, jako je **Cena** = *10* a **Cenové množství** = *3*, protože vytvoří jednotkovou standardní cenu 3.333333 (kde se opakuje desetinná hodnota).
- Ve většině dokumentů nepoužívejte více řádků, které obsahují stejnou kombinaci dimenzí produktů a finančních zásob.
- Snižte stupeň paralelizace. (V tomto případě se systém může zrychlit, protože dojde k menšímu počtu konfliktů a opakování aktualizací.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]