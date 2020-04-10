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
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140368"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Zaznamenání faktury dodavatele do deníku faktur

[!include [banner](../../includes/banner.md)]

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

