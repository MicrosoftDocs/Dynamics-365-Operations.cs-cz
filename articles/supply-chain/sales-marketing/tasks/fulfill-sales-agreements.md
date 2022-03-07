---
title: Plnění prodejních smluv
description: Tento postup popisuje, jak plnit prodejní smlouvy přidružením prodejní objednávky.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e447cbf3d9780b3ccfccbbb065f9b6626d541dd119c733eb800ac285e1bbb0d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713536"
---
# <a name="fulfill-sales-agreements"></a>Plnění prodejních smluv

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak plnit prodejní smlouvy přidružením prodejní objednávky. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Před spuštěním této příručky, zkontrolujte, že máte platnou prodejní smlouvu typu „Závazek – hodnota produktu“. Případně můžete spustit průvodce úkoly nazvaného „Vytvořit prodejní smlouvy“.  




## <a name="release-a-sales-order-from-the-agreement"></a>Vydání prodejní objednávky ze smlouvy
1. Přejděte na Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy.
2. V seznamu otevřete smlouvu, pro kterou chcete vydat objednávku.
3. V podokně akcí klepněte na možnost Prodejní smlouva.
4. Klepněte na Dílčí objednávka.
    * Jak text v horní části stránky Vytvořit dílčí objednávku bodů zdůrazňuje, podrobnosti požadované pro řádky prodejní objednávky se budou lišit podle toho, zda je dohoda založená na množství nebo na hodnotě.  
    * Smlouva v této příručce je typu „Závazek – hodnota produktu“. Proto je oddíl Řádky na této stránce prázdný. Pokud by se závazek zakládal na množství, informace řádku by byly zkopírovány ze smlouvy.  
5. Klikněte na položku Vytvořit.
    * Zpráva vás informuje o tom, že prodejní objednávka byla vytvořena. Objednávka neobsahuje žádné řádky, a proto je proces uvolnění nutné dokončit přidáním podrobností řádku objednávky.   
6. Zavřete stránku.
7. Zavřete stránku.
8. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
9. V seznamu vyhledejte a otevřete objednávku, která byla vytvořena jako výsledek vydání objednávky v předchozí úloze.
10. Klikněte na Přidat řádek.
11. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
12. Do pole Číslo zboží zadejte nebo vyberte zboží, které je zadáno v přidružené prodejní smlouvě.
13. Zadejte číslo do pole Množství.
    * Ujistěte se, že jste zadali množství, které povede k čisté částce pod hodnotou přidružené prodejní smlouvy.  
    * Všimněte si, že když prodejní objednávka je propojena se smlouvou, procento dohodnuté slevy bude použita v řádku objednávky.  
14. Klikněte na položku Aktualizovat řádek.
15. Klikněte na položku Připojeno.
    * Na stránce připojené smlouvy se zobrazí ID a podmínky smlouvy, ze kterých je řádek vydán.  
16. Zavřete stránku.
17. V podokně akcí klikněte na položku Obecné.
18. Klepněte na Připojená prodejní smlouva.
19. Rozbalte sekci Podrobnosti řádku.
20. Klepněte na kartu Plnění.
    * Karta Plnění zobrazuje přehled všech řádků prodejní objednávky, které souvisejí s tímto závazkem a jejich stavem plnění, jakož i částkou nebo množstvím, které ještě nebyly vydány.   
21. Zavřete stránku.
22. Zavřete stránku.
23. Zavřete stránku.

## <a name="apply-sales-agreement-in-the-order-process"></a>Použití prodejní smlouvy v procesu objednávky
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. V seznamu vyhledejte a vyberte odběratele určeného v prodejní smlouvě.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte sekci Obecné.
7. V poli ID prodejní smlouvy klepněte na tlačítko rozevíracího seznamu a otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klepněte na tlačítko Ano.
10. Klikněte na tlačítko OK.
11. Označte v seznamu vybraný řádek.
12. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Do pole Číslo zboží zadejte nebo vyberte zboží, které je zadáno v přidružené prodejní smlouvě.
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. Klepněte na tlačítko Uložit.
16. V podokně akcí klikněte na položku Vyskladnit a zabalit.
17. Klikněte na položku Zaúčtovat dodací list.
18. Rozbalte sekci Parametry.
19. Vyberte možnost Ano v poli Účtování.
20. Klikněte na tlačítko OK.
21. Klikněte na tlačítko OK.
22. V podokně akcí klikněte na položku Obecné.
23. Klepněte na Připojená prodejní smlouva.
24. Klepněte na kartu Plnění.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]