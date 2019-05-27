---
title: Zaznamenání faktury dodavatele do deníku faktur
description: Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556321"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Zaznamenání faktury dodavatele do deníku faktur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami. Mezi příklady tohoto typu faktury patří výdaje pro dodávky nebo služby.  Tento záznam používá ukázkovou společnost USMF.

1. Přejděte na Závazky > Pracovní prostory > Záznam faktury dodavatele.
2. Klikněte na Nový deník faktur.
3. Klikněte na položku Nová.
4. V poli Název zadejte název deníku nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klikněte na položku Řádky.
    * V poli Datum zadejte datum zaúčtování, které provede aktualizaci hlavní knihy.  
7. V poli Účet vyberte účet dodavatele.
8. Do pole Faktura zadejte číslo faktury.
9. Zadejte hodnotu do pole Popis.
10. V poli Dobropis zadejte číslo.
11. V poli Protiúčet zadejte číslo účtu nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání
    * Skupina prodejní daně bude používat výchozí údaje z účtu dodavatele.  
    * Skupina DPH položky bude používat výchozí údaje z hlavního účtu určeného v poli Protiúčet.  
    * Datum splatnosti bude vypočteno na základě platebních podmínek.  
    * Platební sleva bude používat výchozí údaje z účtu dodavatele.  
12. Klikněte na položku Zaúčtovat.
13. Zavřete stránku.

