---
title: Ruční odsouhlasení dopravného
description: Tato procedura ukazuje, jak ručně odsouhlasit dopravné.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838507"
---
# <a name="reconcile-freight-manually"></a>Ruční odsouhlasení dopravného

[!include [banner](../../includes/banner.md)]]

Tato procedura ukazuje, jak ručně odsouhlasit dopravné. To obvykle provádí koordinátor přepravy. Tento postup můžete projít v ukázkových datech společnosti USMF.


## <a name="select-a-load-to-reconcile"></a>Výběr nákladu k odsouhlasení
1. Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.
2. Zrušte zaškrtnutí políčka Skrýt expedované a přijaté. 
3. V seznamu vyberte náklad s ID 00006.

## <a name="create-a-carrier-invoice"></a>Vytvoření faktury dopravce
Pokud ručně odsouhlasíte dopravné a neobdrželi jste automaticky faktury dopravce, můžete vytvořit fakturu založenou na účtu dopravného.  
1. Klepněte na položku Související informace.
2. Klikněte na Zobrazit podrobnosti účtu dopravného.
3. Klikněte na Generovat fakturu za dopravné.
4. Zadejte hodnotu do pole Faktura.
5. Klikněte na tlačítko OK.

## <a name="reconcile-the-invoice"></a>Odsouhlasení faktury
Odsouhlasení faktury dopravce a účtu dopravného provádíte řádek po řádku.  
1. Klikněte na Spárovat účty dopravného a faktury.
2. Rozbalte část Podrobnosti faktury.
3. Rozbalte oddíl Podrobnosti nespárovaného účtu dopravného.
4. Označte na seznamu vybraný řádek.
5. Klepněte na tlačítko Spárovat.
6. Rozbalte oddíl Podrobnosti spárovaného účtu dopravného.

## <a name="submit-the-invoice-for-approval"></a>Odeslat fakturu ke schválení
1. Klikněte na Odeslat ke schválení.
2. Zavřete stránku.
3. Zrušte zaškrtnutí políčka Skrytí schváleno. 
4. Klikněte na Deníky faktur dodavatele.
5. Klepnutím přejdete na odkaz v poli Číslo referenčního deníku.
6. Klikněte na položku Řádky.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]