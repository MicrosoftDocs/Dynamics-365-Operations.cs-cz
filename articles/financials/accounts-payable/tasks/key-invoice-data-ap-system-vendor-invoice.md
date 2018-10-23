--- 
title: "Zadání dat faktur do systému závazků pomocí faktury dodavatele"
description: "Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování)."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a>Zadání dat faktur do systému závazků pomocí faktury dodavatele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Najděte dodavatele, kterého chcete vybrat. Například přejděte na US-104.
5. Vyberte dodavatele US-104.
6. Klepněte na tlačítko OK.
7. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyberte skladovou položku. Například vyberte číslo položky 1000.
9. Rozbalte nebo sbalte oddíl Podrobnosti řádku.
10. Klikněte na záložku Nastavení.
    * Zásady párování je možné přepsat a párování nepoužít, nebo použít dvoucestné či třícestné párování.  
11. Rozbalte nebo sbalte oddíl Podrobnosti řádku.
12. V podokně akcí klikněte na položku Nákup.
13. Klikněte na tlačítko Potvrdit.

## <a name="receive-the-products"></a>Příjem produktů
1. V podokně akcí klikněte na položku Přijmout.
2. Klikněte na položku Příjemka produktu.
3. V poli Příjemka produktu zadejte číslo příjemky produktu. Zadejte například PR123.
4. Kliknutím na tlačítko OK zaúčtujte příjemku produktu.
5. Zavřete stránku.

## <a name="create-a-vendor-invoice"></a>Vytvoření faktury dodavatele
1. Přejděte na Závazky > Nákupní objednávky > Přijaté nákupní objednávky, které nejsou fakturované.
2. Vyberte nákupní objednávku, kterou jste vytvořili.
3. V podokně akcí klikněte na možnost Faktura.
4. Klepněte na Faktura.
5. Do pole Číslo zadejte číslo faktury.
6. Do pole Popis faktury zadejte nějakou hodnotu.
7. Do pole Datum faktury zadejte datum.
8. Zadejte číslo 1200 do pole Jednotková cena.
9. Klikněte na Přidat řádek.
10. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. V seznamu najděte číslo položky pro instalační náklady. Například S0001
12. Vyberte číslo položky pro instalační náklady.
    * Všimněte si, že od okamžiku, kdy jste změny provedli, nebylo provedeno párování.  
13. Klikněte na položku Aktualizovat stav párování.
14. V podokně akcí klikněte na položku Přehled.
15. Klikněte na položku Párování – podrobnosti.
    * Nový řádek se službami se nemusí párovat a stav tak uvádí Neprovedeno.  
16. Vyberte příjemku produktu pro skladovou položku, kterou jste obdrželi.
    * Řádek s příjemkou produktu byl spárován, ale neodpovídá množství nebo cena, a proto došlo k chybě.  
17. Zadejte číslo do pole Jednotková cena.
    * Když nyní odpovídá jednotková cena, stav se aktualizuje na Úspěch. Pokud zásady umožňují nesrovnalosti nebo pokud párování plní pouze funkci upozornění, lze fakturu přesto zaúčtovat.  
18. Zavřete stránku.
19. Klikněte na položku Zaúčtovat.
20. Zavřete formulář.
    * Všimněte si, že nákupní objednávka již není uvedena jako přijatá a nefakturovaná.  


