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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227129"
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
12. Pokud jste povolili workflow deníku faktur dodavatele, klikněte na **Pracovní postup> Odeslat**.
    * Po schválení vašeho odeslání bude datum posunuto na první den následujícího otevřeného období, pokud datum zaúčtování transakce spadá do období, které je pozdrženo nebo uzavřeno pro zaúčtování hlavní knihy.
12. Klikněte na možnost **Zaúčtovat**.
13. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]