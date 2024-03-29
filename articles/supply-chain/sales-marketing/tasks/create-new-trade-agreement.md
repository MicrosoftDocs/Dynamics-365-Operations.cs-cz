---
title: Vytvoření nové obchodní smlouvy
description: Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24290ec873da9e871c001bcdc97e14dcad0e3d1e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111100"
---
# <a name="create-a-new-trade-agreement"></a>Vytvoření nové obchodní smlouvy

[!include [banner](../../includes/banner.md)]

Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Při použití vlastních dat před zahájením tohoto průvodce ověřte, že existuje název deníku obchodních smluv, kde je výchozí vztah je nastaven na „Cena (prodej)“.

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Vytvoření a zaúčtování nového deníku obchodní smlouvy

1. Přejděte do **navigačního podokna > Moduly > Prodej a marketing > Ceny a slevy > Deníky smluv o obchodu**.
2. Klepněte na možnost **Nový**.
3. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. V **podokně akcí** klikněte na možnost **Řádky**.
6. V poli **Kód účtu** vyberte možnost Tabulka.
    
    V tomto příkladu aktualizujete cenu pro určitého odběratele, což znamená, že je nutné vybrat tabulku. Pokud byste aktualizovali katalogovou cenu produktu, vybrali byste Vše, aby nová cena platila pro všechny odběratele. Pokud byste používali různé ceny v různých segmentech odběratelů, vybrali byste možnost Skupina. Chcete-li vybrat skupinu, musíte nastavit možnost Cenové skupiny odběratele.  

7. V poli **Výběr účtu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. V poli **Kód položky** vyberte položku Tabulka.
    
    Při zadávání typu obchodní smlouvy Cena (prodej) je nutné vybrat pouze „Tabulka“ v poli **Kód položky**. Důvodem je skutečnost, že cena je absolutní hodnota a nesmí být stejná pro všechny produkty nebo skupinu produktů.
    
10. V poli **Vztah položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. V seznamu vyberte produkt, který chcete do smlouvy zahrnout. Poznamenejte produkt, který jste vybrali.  
12. V poli **Od** zadejte minimální množství.
    - Pokud odběratel musí objednávat minimální množství, je třeba zde zadat množství, jinak nebude mít na novou cenu nárok.  
    - Zadáním hodnoty do pole **Do** určete maximální množství, nad které nebude cena ve smlouvě platit. Pokud nabízíte ceny a slevy založené na několika množstevních kategoriích, zadejte každou množstevní kategorii jako pár minimálního a maximálního množství do polí **Od** a **Do**.
13. Zadejte cenu do pole **Částka v měně.**
14. V části **Detaily** zadejte do pole **Od data** datum, od kterého bude tato smlouva platná.
15. Klikněte na možnost **Uložit**.
16. Klikněte na tlačítko **Ověřit**.
17. Klikněte na možnost **Ověřit vybrané řádky.**
18. Klikněte na tlačítko **OK**.
19. Klikněte na možnost **Zaúčtovat**.
20. Klikněte na tlačítko **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Zobrazení obchodních smluv pro produkt

1. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
2. V seznamu najděte a vyberte produkt, jehož cenu jste právě aktualizovali.
3. V **podokně akcí** klikněte na možnost **Prodej**.
4. Klikněte na možnost **Zobrazit obchodní smlouvy**.
    
    Zkontrolujte podrobnosti obchodní smlouvy o cenách, kterou jste právě vytvořili.

5. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

### <a name="whitepaper"></a>Dokument Whitepaper

Chcete-li získat další informace, stáhněte si následující dokument whitepaper (napsaný na podporu AX2012, ale stále platí pro Dynamics 365 Supply Chain Management)

- [Obchod. smlouvy](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Blogy komunity

- [Prodejní ceny ve financích a provozu](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
