---
title: Zaznamenání faktury dodavatele do deníku faktur
description: Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837005"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Zaznamenání faktury dodavatele do deníku faktur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami. Mezi příklady tohoto typu faktury patří výdaje pro dodávky nebo služby.  Tento záznam používá ukázkovou společnost USMF.

1. Přejděte na **Navigační podokno > Moduly > Závazky > Pracovní prostory > Záznam faktury dodavatele**.
2. V **Podokně akcí** klikněte na možnost **Nový deník faktur**.
3. Klepněte na možnost **Nový**.
4. V poli **Název** zadejte název deníku nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Zadejte hodnotu do pole **Popis**.
6. V **Podokně akcí** klikněte na **Řádky**. V poli **Datum** zadejte datum zaúčtování, které provede aktualizaci hlavní knihy.  
7. V poli **Účet** vyberte **Účet dodavatele**.
8. Do pole **Faktura** zadejte číslo faktury.
9. Zadejte hodnotu do pole **Popis**.
10. V poli **Dobropis** zadejte číslo.
11. V poli **Protiúčet** zadejte číslo účtu nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání
    * **Skupina prodejní daně** bude používat výchozí údaje z účtu dodavatele.  
    * **Skupina DPH položky** bude používat výchozí údaje z hlavního účtu určeného v poli **Protiúčet**.  
    * **Datum splatnosti** bude vypočteno na základě platebních podmínek.  
    * **Platební sleva** bude používat výchozí údaje z účtu dodavatele.  
12. Klikněte na možnost **Zaúčtovat**.
13. Zavřete stránku.

