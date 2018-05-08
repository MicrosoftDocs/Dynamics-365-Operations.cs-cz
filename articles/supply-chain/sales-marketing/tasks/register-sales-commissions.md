--- 
title: "Registrace prodejních provizí"
description: "Tento postup popisuje, jak jsou vypočítány a registrovány prodejní provize."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Registrace prodejních provizí

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak jsou vypočítány a registrovány prodejní provize. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Před spuštěním této příručky, spusťte průvodce s názvem „Nastavení pravidel prodejní provize“ abyste měli všechna nezbytná nastavení výpočtu provize.

Poznamenejte si čísla odběratele a zboží, které jste zvolili pro proces provize a použijte je, když budete v této příručce vyzváni k vytvoření prodejní objednávky.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Faktura prodejní objednávky, která opravňuje prodejce získat provizi
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na tlačítko OK.
7. V podokně akcí klikněte na Možnosti.
8. Klikněte na tlačítko Změnit zobrazení.
9. Klikněte na možnost Zobrazení záhlaví.
10. Rozbalte sekci Nastavení.
    * Hodnota v poli Prodejní skupina představuje skupinu s jedním nebo více přiřazenými prodejními zástupci. Uživatelé ve skupině jsou ti, kteří po vyfakturování objednávky podle předdefinované sazby a distribuce obdrží provizi.   Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.  Skupina prodeje se zkopíruje také do řádku prodejní objednávky. Můžete ji změnit tak, že se může lišit od skupiny uvedené v záhlaví a/nebo mezi řádky.  
    * Hodnota v poli skupiny provize představuje skupinu, kterou jste vytvořili pro jednoho nebo více odběratelů za účelem sledování provizí.   Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.   
11. V podokně akcí klikněte na Možnosti.
12. Klikněte na tlačítko Změnit zobrazení.
13. Klepněte na možnost Řádkové zobrazení.
14. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. V seznamu vyberte položku, kterou jste pro provize nastavili. 
16. Zadejte číslo do pole Množství.
    * Udělejte si poznámku o řádku Čistá částka. Ta představuje výnosy z prodeje, které v tomto příkladu jsou základem pro výpočet provize.  
17. Klikněte na položku Uložit.
18. V podokně akcí klikněte na položku Faktura.
19. Klikněte na položku Faktura.
20. Rozbalte sekci Parametry.
21. V poli Množství vyberte možnost Vše.
22. Vyberte možnost Ano v poli Účtování.
23. Klikněte na tlačítko OK.
24. Klikněte na tlačítko OK.
    * Zaúčtování transakce může trvat kolem minuty. K dokončení povolte zpracování a nezavírejte stránku.  

## <a name="review-the-registered-sales-commissions"></a>Zobrazení registrovaných provizí z prodeje
1. V podokně akcí klikněte na položku Faktura.
2. Klikněte na položku Faktura.
3. V podokně akcí klikněte na položku Faktura.
4. Klepněte na Transakce provizí.
    * Na kartě Přehled jsou zobrazeny řádky představující částky provize vyplacené prodejním zástupcům, kteří jsou přiřazeni k vyfakturované prodejní objednávce. Zkontrolujme si podrobnosti.     
    * Pokud jste použili průvodce „Nastavení pravidel prodejní provize“ k nastavení prodejní skupiny, existují dva prodejci, kteří obdrží provizi, a provize bude mezi nimi rozdělena stejnoměrně.  
    * V tomto příkladu se vypočítává celková částka provize jako procento výnosu z prodeje (čistá částka řádku objednávky).   
5. Zavřete stránku.
6. Klikněte na možnost Doklad.
    * Transakce dokladu můžete zkontrolovat pro částky provize, které byly zaúčtované do předdefinovaných výdajů a účtů vyplacené provize.  


