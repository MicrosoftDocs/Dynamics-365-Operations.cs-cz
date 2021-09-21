---
title: Konflikt aktualizace nastává, když metoda ocenění zásob je buď standardní cena nebo klouzavý průměr
description: Konflikt aktualizace nastane, když metoda ocenění zásob je buď standardní cena nebo klouzavý průměr
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475826"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Konflikt aktualizace nastane, když metoda ocenění zásob je buď standardní cena nebo klouzavý průměr

## <a name="symptoms"></a>Příznaky

Když paralelně zaúčtujete dokumenty, jako jsou deníky zásob, faktury za nákupní objednávky nebo faktury od prodejní objednávky, kvůli škálovatelnosti a výkonu, může se zobrazit chybová zpráva o konfliktu aktualizací a některé dokumenty se nemusí zaúčtovat. Tento problém nastane, když metoda ocenění zásob je buď *Standardní cena* nebo *Klouzavý průměr*. Obě tyto metody jsou metody stálého výpočtu nákladů. Jinými slovy, konečná cena je stanovena v době zveřejnění.

Pokud používáte metodu *Klouzavý průměr*, chybová zpráva se podobá tomuto příkladu:

> Po výpočtu proporcionálních výdajů se neočekává hodnota zásob xx.xx

Pokud používáte metodu *Standardní náklady*, chybová zpráva se podobá tomuto příkladu:

> Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci. Hodnota = xx.xx, množství = rr.rr, standardní cena = zz.zz

## <a name="workaround"></a>Alternativní řešení

Dokud společnost Microsoft nevydá řešení k vyřešení problému, zvažte použití následujících řešení, která vám pomohou těmto chybám zabránit nebo je snížit:

- Znovu odešlete chybné dokumenty.
- Vytvářejte dokumenty, které mají méně řádků.
- Ve standardní ceně se vyhněte desítkovým hodnotám. Zkuste definovat standardní cenu tak, aby pole **Cenové množství** bylo nastaveno na *1*. Pokud musíte zadat hodnotu **Cenové množství**, která je větší než *1*, zkuste minimalizovat počet desetinných míst v jednotkové standardní ceně. (V ideálním případě by měla být méně než dvě desetinná místa.) Například se vyhněte definování standardního nastavení nákladů, jako je **Cena** = *10* a **Cenové množství** = *3*, protože vytvoří jednotkovou standardní cenu 3.333333 (kde se opakuje desetinná hodnota).
- Ve většině dokumentů nepoužívejte více řádků, které obsahují stejnou kombinaci dimenzí produktů a finančních zásob.
- Snižte stupeň paralelizace. (V tomto případě se systém může zrychlit, protože dojde k menšímu počtu konfliktů a opakování aktualizací.)
