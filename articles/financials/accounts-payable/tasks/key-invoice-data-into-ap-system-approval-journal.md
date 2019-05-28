---
title: Zadání dat faktur do systému závazků pomocí deníku schválení
description: Tento průvodce úkolem popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550367"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Zadání dat faktur do systému závazků pomocí deníku schválení

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.


## <a name="create-and-post-and-invoice"></a>Vytvoření a zaúčtování faktury
1. Přejděte na Závazky > Faktury > Registr faktur.
2. Klikněte na položku Nová.
3. Vyberte název registru faktury, který chcete použít.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Kliknutím na Řádky otevřete registr a zadejte řádky výdajů.
6. Vyberte dodavatele. Například zadejte nebo vyberte možnost US-104
7. Zadejte hodnotu do pole Faktura.
8. Zadejte hodnotu do pole Popis.
9. V poli Dobropis zadejte číslo.
10. V poli Schválil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyberte schvalujícího a kliknutím na tlačítko Vybrat tohoto schvalovatele vyberte.
12. Klikněte na položku Zaúčtovat.
13. Zavřete stránku.
14. Zavřete stránku.

## <a name="approve-an-invoice"></a>Schválení faktury
1. Přejděte na Závazky > Faktury > Schválení faktury.
2. Klikněte na položku Nová.
3. Vyberte název deníku schválení faktur, který chcete použít.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Kliknutím na položku Řádky zobrazte stránku, kde bude možné vybrat faktury, které chcete schválit.
6. Výběrem možnosti Hledat doklady zobrazte všechny faktury, které jsou již připraveny ke schválení.
7. Označte fakturu, kterou jste vytvořili.
8. Klepněte na tlačítko Vybrat.
    * Doklady vybrané výše, se po výběru přesunou do tohoto seznamu.  
9. Klikněte na tlačítko OK.
10. Klepnutím na pole číslo účtu přidejte výdajový účet k faktuře.
11. Zadejte číslo účtu a opusťte toto pole. Například zadejte „600120“.
12. Klikněte na položku Zaúčtovat.
13. Kliknutím na tlačítko Doklad zobrazte položky, které byly zaúčtovány.
    * Účet Faktury čekající na schválení bude stornován a nahrazen údaji skutečného účtu výdajů.  

