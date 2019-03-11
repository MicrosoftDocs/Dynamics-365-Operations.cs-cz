---
title: Expedování prodejních objednávek bez skladování
description: Tato příručka ukazuje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "312961"
---
# <a name="ship-sales-orders-without-warehousing"></a>Expedování prodejních objednávek bez skladování

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato příručka ukazuje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli. Průvodce lze použít pro tok plnění, který není nastaven pro správu skladu (ani základní ani rozšířené funkce skladu), a proto nevyžaduje zaregistrování výdeje produktu mají před dodávkou. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. V obou případech před spuštěním této úlohy vytvořte prodejní objednávku pro produkt na skladě s množstvím větším než 1. Abyste předešli chybě zaúčtování, je třeba zkontrolovat, že množství produktu na skladě na pracovišti a ve skladu, které jste vybrali na objednávce, zahrnuje množství objednávky.


## <a name="post-packing-slip-for-an-order"></a>Zaúčtování dodacího listu pro objednávku
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. V seznamu vyhledejte a vyberte objednávku, kterou jste vytvořili pro tento úkol.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na tlačítko Vyskladnit a zabalit.
5. Klikněte na Zaúčtovat dodací list.
6. Rozbalte nebo sbalte oddíl Parametry.
7. V poli Množství vyberte možnost Vše.
    * Ostatní možnosti zahrnují Dodat nyní a Vyskladněno. Pokud řádek objednávky má být částečně dodán a pole Dodat nyní v řádku objednávky obsahuje nějaké množství, vybrali byste Dodat nyní. Pokud tok plnění vaší organizace zahrnuje výdej jako samostatný proces, který je spravován a zaregistrován ve výdejce, měli byste vybrat Vyskladněno.  
    * Zkontrolujte, zda je Možnost zaúčtování nastavena na hodnotu Ano.  
8. Nastavte možnost Tisk dodacího listu na Ano.
    * Karta Přehled obsahuje seznam dodacích listů k vygenerování v tomto zaúčtování. Pokud dodáváte jednotlivé objednávky, obvykle bude jeden dodací list. Avšak jsou-li řádky objednávky, která má být expedována, z různých pracovišť, zaúčtování bude automaticky rozděleno na příslušný počet dokumentů. Jedná se o povinnou podmínku, kterou nelze změnit. Obdobně platí, že zaúčtování bude rovněž rozděleno do několika dokumentů, pokud mají řádky objednávky k dodání různé doručovací adresy a nastavení zásad expedice vyžaduje rozdělení.  
9. Na kartě Řádky vyberte řádek pro řádek objednávky k expedici.
10. V poli Aktualizace zadejte číslo menší než původní množství.
11. Klikněte na tlačítko OK.
12. Klepněte na tlačítko Ano.
13. Zavřete stránku.
14. V podokně akcí klikněte na Možnosti.
15. Klikněte na tlačítko Změnit zobrazení.
16. Klikněte na možnost Zobrazení záhlaví.
    * Pokud byly plně expedovány všechny řádky objednávky, stav zakázky se změní z otevřeného na dodáno.  
    * V tomto případě byl řádek objednávky expedován částečně. Toto je důvod, proč stav objednávky zůstane otevřený.     
    * Pole Stav dokumentu je nastaveno na Dodací list, protože alespoň jeden z řádků objednávky byl dodán.  
17. V podokně akcí klikněte na položku Obecné.
18. Klepněte na Množství řádků.
19. Zavřete stránku.
20. V podokně akcí klikněte na položku Vyskladnit a zabalit.
21. Klepněte na Dodací list.
    * Stránka deníku dodacího listu obsahuje všechny dokumenty dodacího listu, které byly vygenerovány pro vaši objednávku. Můžete zkontrolovat podrobnosti o jednotlivých dokumentech a vytisknout je, pokud chcete.  

