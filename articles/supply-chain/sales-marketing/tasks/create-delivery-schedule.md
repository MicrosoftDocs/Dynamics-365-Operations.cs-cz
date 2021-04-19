---
title: Vytvoření plánu dodávek
description: Tento postup ukazuje, jak vytvořit plán dodávek pro prodejní objednávku.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79fa41df07bc09f24e31900a52f4905db6d1c63e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836415"
---
# <a name="create-delivery-schedule"></a>Vytvoření plánu dodávek

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak vytvořit plán dodávek pro prodejní objednávku. Plán dodávek se používá, pokud množství z objednávky nebo nabídky má být dodáno v podobě vícenásobné expedice. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-delivery-schedule"></a>Vytvoření plánu dodávek
1. Přejděte na Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
4. Klepněte na tlačítko OK.
5. V poli Číslo zboží zadejte nebo vyberte hodnotu.
6. Do pole Množství zadejte číslo, které je větší než 1.
7. Klikněte na položku Řádek prodejní objednávky.
8. Klikněte na položku Plán dodávek.
    * Stránka Plán dodávek je místo, kde můžete zadat počet dodávek, ve kterých budou dodány celková množství řádku objednávky pro odběratele.    
    * Ve výchozím stavu systém zkopíruje celkové množství a další podrobnosti o původním prodejním řádku na první řádek plánu dodávek. V tomto příkladu vytvoříme plán na dvě dodávky s posunem data druhé dodávky o týden od první.  
9. Do pole Množství zadejte číslo, které je částí celkového množství.
10. Klepněte na možnost Nový.
11. V poli Množství zadejte zbývající množství.
12. Do pole Požadované datum expedice zadejte datum, které je jeden týden před datem dodání prvního řádku.
    * Dvě možnosti na pevné záložce Převod nákladů řídí způsob, jakým chcete poplatky distribuovat napříč řádky plánu dodávek po jejich přiřazení na řádek původní objednávky. Pokud vyberete Kopírovat hrubé částky, stejná částka nákladů se zkopíruje do každého řádku. Možnost Přidělit řádkům dodávek umožňuje dělit náklady rovnoměrně mezi řádky dodávky.  
    * Rozdělit lze jen pevné náklady, zatímco variabilní náklady se stále budou kopírovat do řádků.  
13. Přesuňte kurzor od druhého řádku dodání, pokud chcete stránku aktualizovat.
    * Je možné sledovat celkové množství, která je přiděleno na řádky plánu dodávek tím, že si prohlédnete pole Součet a Zbývající. Pokud je zbývající množství nulové, bylo do plánu přiděleno celé množství z původního řádku.   
14. Klikněte na tlačítko OK.
    * Plán dodávek byl nyní zkopírován do řádků objednávky.   
    * Původní řádek objednávky označovány jako obchodní řádek byl předveden na řádek objednávky s více dodávkami. Je označen jedinečnou ikonou a chová se jako záhlaví pro řádky dodávky.  
    * Dva nové řádky, označované jako řádky dodávky, tvoří jeden plán dodávek. Objednávka bude zpracována s ohledem na tyto řádky, nikoli na původní řádek. Pokud jsou vytištěny dokumenty, jako například doklady pro potvrzení, výdejky, dodací listy nebo faktury, budou zobrazeny pouze řádky dodávky.   
    * Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze uskladnění, jako například pracoviště a sklad. Dimenze produktu však musí vždy souhlasit s údaji na obchodním řádku a nelze je změnit.  
15. Do pole Množství zadejte číslo, které je větší než současné.
16. Vyberte obchodní řádek a prohlédněte si jeho vliv na přepočítání množství.
17. V podokně akcí klikněte na položku Vyskladnit a zabalit.
18. Klikněte na Zaúčtovat dodací list.
19. Rozbalte sekci Parametry.
20. V poli Množství vyberte možnost Vše.
    * Mějte na paměti, že dodací list bude vytvořen pro dva řádky plánu dodávek a nikoli pro původní řádek objednávky.  
21. Vyberte možnost Ano v poli Tisk dodacího listu.
22. Klikněte na tlačítko OK.
23. Klepněte na tlačítko Ano.
24. Zavřete stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]