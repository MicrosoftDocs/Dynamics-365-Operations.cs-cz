---
title: Úprava úrovně zásob ve skladu (základní správa skladu)
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku úpravy zásob za účelem úpravy úrovně zásob produktu ve skladu.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834138"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Úprava úrovně zásob ve skladu (základní správa skladu)

[!include [banner](../../includes/banner.md)]

Tento postup vás provede procesem vytvoření a zaúčtování deníku úpravy zásob za účelem úpravy úrovně zásob produktu ve skladu. Předtím, než začnete, je třeba mít nastaven název deníku zásob pro úpravy zásob. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Tyto úkoly obvykle provádějí zaměstnanci skladu.


## <a name="create-an-inventory-adjustment-journal"></a>Vytvoření deníku úprav zásob
1. Přejděte do Řízení zásob > Položky deníku > Zboží > Úprava zásob.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. V seznamu klepněte na název deníku úpravy skladu, který chcete použít.
    * Některá další pole budou vyplněna na základě nastavení názvu deníku úprav zásob, který jste vybrali.  
5. Klikněte na tlačítko OK.

## <a name="create-journal-lines"></a>Vytvoření řádků deníku
1. Klikněte na položku Nová.
2. V seznamu označte pole čísla položky.
3. V poli Číslo položky vyberte položku. Používáte-li ukázková data společnosti USMF, zadejte hodnotu „D0001“.
4. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V seznamu vyberte web.
6. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. V seznamu vyberte sklad.
    * Pokud jste vybrali položku se skladovým místem jako povinnou dimenzi, je zde třeba určit umístění.  
8. Zadejte číslo do pole Množství.
    * Pole nákladové ceny určuje náklady za jednotku za příjmy na sklad. Pokud náklady nejsou pro číslo položky specifikovány nebo pokud je chcete určit ručně, lze to udělat zde.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Proveďte ověření a zaúčtování deníku úprav zásob.
1. Klikněte na tlačítko Ověřit.
2. Klikněte na tlačítko OK.
3. Klikněte na položku Zaúčtovat.
    * Když tento typ deníku zaúčtujete, zaúčtuje se příjem nebo výdej zásoby, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.  
4. Klikněte na tlačítko OK.
5. Zavřete formulář.
6. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]