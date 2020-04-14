---
title: Vytvoření nákupní objednávky z prodejní objednávky
description: Tento postup zobrazuje, jak vytvořit nákupní objednávku na základě plánu prodejní objednávky.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30ffb34e2aee984d29bedb47d6bfc9cb6173470a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148669"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Vytvoření nákupní objednávky z prodejní objednávky

[!include [banner](../../includes/banner.md)]

Tento postup zobrazuje, jak vytvořit nákupní objednávku na základě plánu prodejní objednávky. Množství produktu na nákupní objednávce je pak označeno k uspokojení poptávky původní prodejní objednávky. Plnění prodejní poptávky tímto způsobem je alternativou k více srozumitelné a optimalizované metodě požadavků plánování distribuce. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Vytvoření nákupní objednávky z prodejní objednávky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. Klepněte na možnost **Nový**.
3. V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na tlačítko **OK**.
6. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Pokud používáte data USMF, můžete vybrat položku D0001.  
8. Zadejte číslo do pole **Množství**.
9. Klikněte na **Přidat řádek**.
10. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Pokud používáte data USMF, můžete vybrat položku T0020.  
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. Zadejte číslo do pole **Množství**.
14. Klikněte na možnost **Uložit**.
15. V **podokně akcí** klikněte na možnost **Prodejní objednávka**.
16. Klikněte na **Nákupní objednávku**. Stránka **Vtvoření nákupní objednávky** obsahuje všechny otevřené řádky prodejních objednávek, které byly zkopírovány z prodejní objednávky. Je možné zkontrolovat podrobnosti o objednávce, a v případě potřeby můžete upravit vybrané informace, například nákupní množství a cenách podmínek předtím, než vytvoříte objednávku. 
17. Vyberte možnost **Zahrnout vše**.
    - Pokud chcete generovat nákupní objednávku pouze pro podmnožinu řádků prodejních objednávek, vyberte je jednotlivě.  
    - Pole **Účet dodavatele** může nebo nemusí být vyplněno číslem dodavatele. Pokud bude výchozí dodavatele nastaven pro produkt (v přidružené disponibilitě položky), pak do řádku bude zkopírován tento dodavatel. V ostatních případech musíte dodavatele zadat ručně.  V této příručce bez ohledu na to, zda pole **Účet dodavatele** již obsahuje hodnotu či nikoli, vám další kroky poradí, jak vybrat nového dodavatele, který se liší pro každý řádek.  
18. V poli **Účet dodavatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
20. Klikněte na odkaz na vybraném řádku v seznamu.
21. Vyberte druhý řádek objednávky.
22. V poli **Účet dodavatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
23. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
24. Klikněte na odkaz na vybraném řádku v seznamu.
25. Klikněte na tlačítko **Ověřit**.
26. Klikněte na tlačítko **OK**. Zpráva vás informuje o tom, že jedna nebo více nákupních objednávek nyní bylo vytvořeno. Systém vygeneruje jednotlivou nákupní objednávku pro každého dodavatele, kterého jste určili pro řádky prodejní objednávky. To znamená, že pokud několik řádků prodejní objednávky má být zásobováno stejným dodavatelem, bude vygenerována jedna nákupní objednávka s více řádky.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Zkontrolujte nákupní objednávky vytvořené z prodejních objednávek.
1. V **podokně akcí** klikněte na **Obecné**.
2. Klikněte na **Související objednávky**. Stránky se seznamem **souvisejících objednávek** všech objednávek, které byly vytvořeny z prodejní objednávky. V tomto příkladu jsou dvě nákupní objednávky, které jsou generovány pro dva různé dodavatele v uvedeném pořadí. 
3. Kliknutím přejdete na odkaz v poli **Nákupní objednávka**. Každý řádek nákupní objednávky je přidružen k řádku prodejní objednávky, který k nákupu vedl. Vztah k prodejní objednávce je označen na **Kartě produktu** na pevné kartě **Podrobnosti řádku** v polích **Typ odkazu**, **Číslo odkazu** a **Odkaz na šarži**.  
4. Rozbalte nebo sbalte oddíl **Podrobnosti řádku**.
5. Klikněte na kartu **Produkt**.
    - **Odkaz na šarži** zajišťuje, že náklady aktuálního nákupu budu zpoplatněny na připojené prodejní objednávce.  
    - Otevřením odkazu v poli **Referenční číslo** můžete přejít na původní prodejní objednávku.  

