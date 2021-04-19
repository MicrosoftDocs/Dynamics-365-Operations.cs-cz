---
title: Odsouhlasení nákladu ve správě přepravy
description: Toto téma popisuje proces odsouhlasení dopravného.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809079"
---
# <a name="reconcile-freight-in-transportation-management"></a>Odsouhlasení nákladu ve správě přepravy

[!include [banner](../includes/banner.md)]

Toto téma popisuje proces odsouhlasení dopravného.

Odsouhlasení dopravného lze provádět ručně, nebo je můžete nastavit automaticky. Chcete-li použít automatické odsouhlasení dopravného, musíte vytvořit předlohu auditu, kde definujete kritéria určující, které účty dopravného jsou spárovány automaticky.

## <a name="the-freight-reconciliation-process"></a>Proces odsouhlasení dopravného

Sazby dopravného se vypočítají podle sazebního modulu, který je spojen s odpovídajícím dopravcem. Po potvrzení nákladu je generován účet dopravného, do kterého jsou přeneseny sazby za přepravu. Sazby za přepravu jsou rozděleny jako vedlejší náklady do příslušného zdrojového dokladu (nákupní objednávky, prodejní objednávky nebo převodní příkaz) v závislosti na nastavení, které se používá pro normální proces fakturace. Proces odsouhlasení dopravného (známý také jako proces spárování) můžete spustit ihned po přijetí faktury dopravného od dopravce. Fakturu lze přijímat elektronicky nebo papírově. Pokud je faktura přijata papírově, může vygenerovat elektronickou fakturu pomocí účtu dopravného coby předlohy.

[![Proces odsouhlasení dopravného](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Ruční odsouhlasení

Pokud provádíte odsouhlasení dopravného ručně, musíte spárovat každý řádek faktury s řádkem/řádky účtu dopravného pro náklad, který se fakturuje. Toto párování provádíte na stránce **Spárování účtů dopravného a faktur**. Pokud částka na řádku faktury neodpovídá částce na účtu dopravného, je nutné vybrat důvod odsouhlasení pro tento rozdíl. Pokud existuje více důvodů k odsouhlasení, je možné rozdělit nespárované částky mezi ně. Důvod odsouhlasení určuje, jak jsou rozdílné částky zaúčtovány v hlavní knize. Pokud zohledňujete odsouhlasení celé fakturované částky, je částka odeslána ke schválení, a následně je zaúčtován deník. Následující obrázek ukazuje, jak generovat fakturu za dopravné a provádět odsouhlasení dopravného.

[![Úlohy odsouhlasení dopravného](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatické odsouhlasení

Chcete-li použít automatické odsouhlasení, je nutné zadat plán odsouhlasení, stejně jako faktury a dopravce, které chcete použít. Párování řádků faktury a účtů dopravného se provádí podle nastavení v hlavním auditu a podle typu účtu dopravného. Po spuštění automatického odsouhlasení musíte zpracovat všechny faktury, které systém nespáruje. Tyto faktury musíte poté ručně zpracovat, než budete moci zaúčtovat všechny faktury pro platbu.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Spárujte přepravní faktury s přepravními fakturami pomocí automatického nebo ručního odsouhlasení

*Párování* je proces hledání účtů za přepravu, které odpovídají každé faktuře za přepravu. To lze provést párováním jednotlivých řádků faktur (ruční párování) nebo párováním všech dostupných faktur najednou (automatické párování).

### <a name="auto-matching"></a>Automatické párování

Při párování více faktur za přepravu se stejným účtem za přepravu funguje proces automatického párování následovně:

1. Všechny faktury za přepravu, které se neshodují, jsou seřazeny podle částky, s největší částkou jako první.
1. Faktury za přepravu se spárují jedna po druhé, dokud na faktuře za přepravu nezůstane žádná kladná částka.
1. V závislosti na nastavení hlavního auditoru a zbývající částky na fakturách za přepravu je nastavena zbývající částka.

### <a name="manual-matching"></a>Ruční párování

Ke spárování budou k dispozici všechny účty za přepravu s kladnými částkami. Podobně jako automatické přiřazování bude uživatel moci pouze spárovat přepravní faktury se zápornými částkami s přepravními doklady, které nejsou plně uzavřeny.

### <a name="example"></a>Příklad

Předpokládejme, že máte přepravní doklad (FB) za částku 1 500 a že jste vytvořili tři přepravní faktury za přepravní doklad s jedním řádkem faktury pro každou fakturu s následujícím nastavením:

- Původní nákladní list (FB): Částka 1 500
- Faktura 1 (Inv1): Částka 1 000
- Faktura 2 (Inv2): Částka 600
- Faktura 3 (Inv3): Částka -100

#### <a name="automatic-matching-result"></a>Výsledek automatického párování

Automatické přiřazování se provede v následujícím pořadí:

1. Seřadit všechny přepravní faktury sestupně podle částky: Inv1 -> Inv2 -> Inv3.
1. Spárujte Inv1 s FB. Inv1 má 1000 spárováno a FB má zbývající částku 500, takže stav je nastaven na *Částečně spárováno*.
1. Spárujte Inv2 s FB. Inv2 má 500 spárováno a FB má zbývající částku 0, takže stav je nastaven na *Plně spárováno*.
1. Protože FB je nyní plně uzavřeno, Inv3 nebude zpracována.

#### <a name="manual-matching-result"></a>Výsledek ručního párování

U ručního párování se výsledky liší v závislosti na pořadí párování, jak je znázorněno v následujících příkladech.

##### <a name="manual-matching-case-1"></a>Ruční párování, případ 1

Jedním ze způsobů ručního párování v tomto příkladu je tento postup:

1. Spárujte FB s Inv1. FB má zbývající částku 500, takže stav je nastaven na *Částečně spárováno*.
1. Spárujte Inv2 s FB. Inv2 má 500 spárováno a FB má zbývající částku 0, takže stav je nastaven na *Plně spárováno*.
1. Když ručně spárujete Inv3, nenajdete žádné nespárované účty za přepravu.

Tento případ je v podstatě stejný jako automatické párování

##### <a name="manual-matching-case-2"></a>Ruční párování, případ 2

Dalším ze způsobů ručního párování v tomto příkladu je tento postup:

1. Spárujte Inv3 s FB. Nyní má FB zbývající částku 1600, což je stejné jako odečtení záporných 100 nad 1500. FB i Inv3 mají shodné množství -100.
1. Spárujte Inv1 a Inv 2 s FB jeden po druhém. FB je plně uzavřeno.

Jak ukazuje tento příklad, párování faktur za přepravu se zápornými částkami by se mělo provádět pouze ručně. Tím zajistíte, že je vždy možné spárovat přepravní faktury se zápornými částkami k přepravnímu dokladu, který není plně uzavřen, protože vám to umožňuje řídit odpovídající sekvenci.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]