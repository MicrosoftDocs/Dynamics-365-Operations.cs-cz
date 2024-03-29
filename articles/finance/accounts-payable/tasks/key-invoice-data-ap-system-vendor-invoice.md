---
title: Zadání dat faktur do systému závazků pomocí faktury dodavatele
description: Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c441d197957674d68c4c92b454a9dca91d76ea0
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775154"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Zadání dat faktur do systému závazků pomocí faktury dodavatele

[!include [banner](../../includes/banner.md)]

Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všechny nákupní objednávky**.
2. Klepněte na možnost **Nový**.
3. V poli **Účet dodavatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Najděte dodavatele, kterého chcete vybrat. Například přejděte na US-104.
5. Vyberte dodavatele US-104.
6. Klikněte na tlačítko **OK**.
7. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyberte skladovou položku. Například vyberte číslo položky 1000.
9. Rozbalte pevnou záložku **Podrobnosti řádku**.
10. Klikněte na kartu **Nastavení**. Zásady párování je možné přepsat a párování nepoužít, nebo použít dvoucestné či třícestné párování.  
11. V podokně akcí klikněte na možnost **Zakoupit**.
12. Klikněte na tlačítko **Potvrdit**.

## <a name="receive-the-products"></a>Příjem produktů
1. V podokně akcí klikněte na možnost **Přijmout**.
2. Klikněte na **Příjemka produktu**.
3. V poli **Příjemka produktu** zadejte číslo příjemky produktu. Zadejte například PR123.
4. Kliknutím na tlačítko **OK** zaúčtujte příjemku produktu.
5. Zavřete stránku.

## <a name="create-a-vendor-invoice"></a>Vytvoření faktury dodavatele
1. V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Přijaté nákupní objednávky, které nejsou fakturované**.
2. Vyberte nákupní objednávku, kterou jste vytvořili.
3. V podokně akcí klikněte na možnost **Faktura**.
4. Klikněte na **Faktura**.
5. Do pole **Číslo** zadejte číslo faktury.
6. Do pole **Popis faktury** zadejte nějakou hodnotu.
7. Zadejte datum do pole **Datum faktury**.
8. Zadejte číslo 1200 do pole **Jednotková cena**.
9. Klikněte na **Přidat řádek**.
10. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. V seznamu najděte číslo položky pro instalační náklady. Například S0001
12. Vyberte číslo položky pro instalační náklady. Všimněte si, že od okamžiku, kdy jste změny provedli, nebylo provedeno párování.  
13. Klikněte na **Aktualizovat stav párování**.
14. V podokně akcí klikněte na položku **Přehled**.
15. Klikněte na položku **Podrobnosti párování**. Nový řádek se službami se nemusí párovat a stav tak uvádí Neprovedeno.  
16. Vyberte příjemku produktu pro skladovou položku, kterou jste obdrželi. Řádek s příjemkou produktu byl spárován, ale neodpovídá množství nebo cena, a proto došlo k chybě.  
17. Zadejte číslo do pole **Jednotková cena**. Když nyní odpovídá jednotková cena, stav se aktualizuje na Úspěch. Pokud zásady umožňují nesrovnalosti nebo pokud párování plní pouze funkci upozornění, lze fakturu přesto zaúčtovat.  
18. Zavřete stránku.
19. Klikněte na možnost **Zaúčtovat**.
20. Zavřete stránku. 

>[!Note] 
>Nákupní objednávka již není uvedena jako přijatá a nefakturovaná.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
