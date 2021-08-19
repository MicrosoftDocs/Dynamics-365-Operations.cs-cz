---
title: Vytvářet prodejní objednávky
description: Tato procedura popisuje způsob vytváření prodejní zakázky.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bf52a90a709aa74c579aa0047a38c1f3c7a845711f61f07a491705c798f1c62
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744075"
---
# <a name="create-sales-orders"></a>Vytvářet prodejní objednávky

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob vytváření prodejní zakázky. Tento postup můžete projít v ukázkových datech společnosti USMF. Prodejní objednávku obvykle vytváří zpracovatel prodejních objednávek. 

## <a name="enter-sales-order-header-details"></a>Zadejte informace ze záhlaví prodejní objednávky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu záznam odběratele a vyberte ho.
    - V tomto příkladu vyberte číslo odběratele US-004.  
5. Vyberte **OK**.

## <a name="enter-sales-order-line-details"></a>Zadejte informace z řádků prodejní objednávky
    
Produkty prodané vaší organizací mohou nabízet více variant rozlišených podle dimenzí, jako je například konfigurace, barva, velikost a styl. Dále produkty lze nastavit tak, aby používaly dimenze uskladnění, jako je například pracoviště, sklad a palety, a sledovací dimenze, jako například dávky nebo sériové číslo. Když jsou tyto dimenze přiřazeny, je nutné vybrat hodnoty pro tyto dimenze na řádku objednávky. Ke zvýšení efektivity zadání objednávky můžete přidat odpovídající pole dimenze do mřížky objednávky.
    
1. V části **řádky prodejní objednávky** vyberte **řádek prodejní objednávky**.
2. Vyberte **Dimenze**.
    
    V tomto příkladu vyberte Barva, Pracoviště a Sklad. Zde zvolené dimenze se zobrazí v mřížce prodejní objednávky. Podle potřeby můžete svůj výběr uchovávat tím, že nastavíte možnost **Uložit nastavení** na hodnotu Ano.
    
3. Vyberte **OK**.
4. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V tomto příkladu vyberte číslo položky T0004.
    - Pokud je položka součástí kategorie prodeje, název položky se automaticky zobrazí v poli Prodejní kategorie.  
    - Pokud pole s dimenzí produktu již obsahuje hodnotu, je to proto, že hodnota byla zkopírována ze záznamu produktu, kde je definována jako výchozí dimenze produktu. Výchozí hodnotu lze kdykoli změnit.   
6. V poli **Barva** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Zadejte číslo do pole **Množství**.
    - Pokud je jednotka prodána v odlišných jednotkách, než ve kterých byla zakoupena, vyrobena a uložena, a měrná jednotka prodeje je nastavena na záznam produktu, tato hodnota se zobrazí v poli **Jednotka**. Hodnotu lze kdykoli změnit.   
    - Pokud pole **Pracoviště** již obsahuje hodnotu, hodnota byla zkopírována ze záhlaví objednávky nebo z nastavení objednávky, která je přidružena k produktu. Hodnotu lze kdykoli změnit. Pokud je pole prázdné, vyberte hodnotu.   
    - Pokud pole **Jednotková cena** již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy nebo ze záznamu produktu. (Jednotková cena může také pocházet z prodejní smlouvy, ale proces vytváření prodejních objednávek z prodejních smluv se liší od toho, který je zobrazen zde.) Pokud je pole prázdné, zadejte hodnotu.   
    - Pole **Sleva** obsahuje částku slevy za každou jednotku produktu. Pokud chcete vypočítat celkovou řádkovou slevu, hodnota slevy bude vynásobena množstvím na řádku. Pokud pole **Sleva** již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy. Pokud je pole prázdné a vy chcete přiřadit odběrateli řádkovou slevu, můžete zadat hodnotu.  
    - Pole **Procento slevy** obsahuje procentuální hodnotu, o kterou má být snížena celková hrubá částka na řádku.  Pokud pole **Procento slevy** již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy. Pokud je pole prázdné a vy chcete přiřadit odběrateli řádkovou slevu, můžete zadat hodnotu. 
    - Pole **Čistá částka** obsahuje hodnotu, která se vypočte podle množství a jednotkové ceny na řádku, upravenou o slevu.  Je možné přepsat vypočtené hodnoty na jiné.  

## <a name="review-the-order-totals"></a>Kontrola součtů objednávky
1. V **podokně akcí** klikněte na položku **Prodejní objednávka**.
2. Vyberte možnost **Součty**.
    
    Stránka **Součty** zobrazí podrobnosti o celé objednávce. Jedná se o mezisoučtu částkou, která představuje součet všech čistých částek na řádku upravených pro případné řádkové slevy, celkovou částku faktury, která tvoří mezisoučet upravený pro případnou slevu na úrovni objednávky, náklady, DPH, situaci limitního úvěru zákazníka apod. Částka faktury je částka, která se zobrazí na dokladu pro fakturu odběratele.  
    
3. Vyberte **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]