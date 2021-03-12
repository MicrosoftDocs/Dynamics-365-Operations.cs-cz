---
title: Vytváření a úpravy prodejních nabídek
description: Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6735b1a538c7e4c82eb57282ab810490baee1923
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974928"
---
# <a name="create-and-edit-sales-quotations"></a>Vytváření a úpravy prodejních nabídek

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-sales-quotation"></a>Vytvoření prodejní nabídky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní nabídky > Všechny nabídky**.
2. Klepněte na možnost **Nový**.
3. V poli **Typ účtu** vyberte „Potenciální zákazník“.
4. V poli **Potenciální zákazník** zadejte nebo vyberte hodnotu.
5. Rozbalte sekci **Obecné**. Vzhledem k tomu, že jste zvolili vytvoření nabídky z oblasti prodeje a marketingu, je typ nastaven automaticky na ‚prodejní nabídku‘. K vytvoření nabídky pro projekt k ní musíte mít přístup z modulu **Řízení a účetnictví projektů**.
6. Klikněte na tlačítko **OK**. Pole a akce pro řádky nabídky se velmi podobají položkám na řádcích prodejní objednávky.   Stejně jako prodejní objednávky lze nabídky vytvářet pro konkrétní zboží nebo pro neznámé či neexistující číslo zboží, které v době vytvoření nabídky není k dispozici, nabídky lze vytvářet pro kategorii prodeje.     
7. V poli **Zboží** zadejte nebo vyberte hodnotu.
8. Zadejte hodnotu do pole **Pracoviště**.
9. Zadejte číslo do pole **Množství**. Pokud existují platné obchodní smlouvy pro vybrané zboží v řádku, použití cena a slevy se automaticky zkopírují řádku nabídky. Ujistěte se, že pole Jednotková cena obsahuje hodnotu a chcete-li můžete také zadat hodnotu slevy. 
10. Klikněte na možnost **Uložit**.
11. V **podokně akcí** klikněte na možnost **Prodejní nabídka**.
12. Klepněte na možnost **Součet**.
13. Klikněte na tlačítko **OK**.
14. Vyberte řádek prodejní nabídky.
15. V **Podokně akcí** klikněte na možnost **Nabídka**.
16. Klikněte na **Simulaci ceny**.
    - Na stránce **Spustit simulaci** ceny můžete vyzkoušet úpravami očekávané výnosy nebo ziskovost vaší nabídky na základě požadované jednotkové ceny, částku slevy, procento slevy, celkovou částku, marži nebo příspěvkový poměr. Pokud jste spokojeni s cílovými hodnotami, lze návrh použít pro daný řádek nabídky a její pole související s cenami bude odpovídajícím způsobem aktualizováno.  
    - Simulací cen můžete vytvářet, kolik chcete. Klepnete-li na **Nový**, cenové podmínky z aktuálního řádku nabídky se zkopírují na stránku. Můžete pak upravit hodnoty v jakémkoli poli souvisejícím s cenami do cílových hodnot. Změny v jednom z polí spustí přepočet ve všech ostatních polích. Aby systém vypočítal prodejní marže a příspěvkový poměr, musí znát pořizovací cenu produktu. Použijte kartu Simulované ceny pro podrobné zobrazení původních cen, navržených změn a jejich vlivu na celkové hodnoty nabídky. Obecně platí, že když simulace určuje nové množství pro daný řádek nabídky, systém přepočítá a zadá novou hodnotu v poli Jednotková cena. Pokud simulace vychází z nové marže nebo nového příspěvkového poměru, je aktualizováno pouze pole Čistá částka a pole Jednotková cena je prázdné. V obou případech budou odstraněny všechny slevy, které byly na řádku nabídky před simulací.
17. V **Podokně akcí** klikněte na možnost **Nabídka**.
18. Klikněte na **Odeslat nabídku**.
19. Vyberte možnost ‚Ano‘ v poli **Tisk nabídky**.
20. Klikněte na tlačítko **OK**. Generování sestavy může trvat několik minut. Dokud proces nebude dokončen, stránku nezavírejte.

## <a name="update-a-sales-quotation"></a>Aktualizace prodejní nabídky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní nabídky > Všechny nabídky**.
2. V **podokně akcí** klikněte na možnost **Zpracování**.
3. Klikněte na **Převést na odběratele**.
4. V poli **Účet odběratele** zadejte hodnotu.
5. Klikněte na možnost **Kontrola**. Ujistěte se, že se zobrazí zpráva, že číslo účtu, které jste zadali, lze volně použít.  
6. Klikněte na tlačítko **OK**. Systém právě vytvořil účet nového odběratele pro potenciálního zákazníka z nabídky.  
7. Zavřete stránku.
8. V **podokně akcí** klikněte na možnost **Zpracování**.
9. Klikněte na tlačítko **Potvrdit**.
10. V poli **Důvod** zadejte nebo vyberte hodnotu.
11. Klikněte na tlačítko **OK**.
12. V **podokně akcí** klikněte na **Obecné**.
13. Klikněte na **Prodejní objednávky**.
14. Zavřete stránku.

