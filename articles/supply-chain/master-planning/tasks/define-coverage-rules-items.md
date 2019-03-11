---
title: Definování pravidel disponibility pro položky
description: K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "320620"
---
# <a name="define-coverage-rules-for-items"></a>Definování pravidel disponibility pro položky

[!include [task guide banner](../../includes/task-guide-banner.md)]

K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup popisuje, jak vytvořit pravidla disponibility a přepsat nastavení disponibility pro určitou položku. Také ukazuje, jak zadat výchozí nastavení skladu.


## <a name="create-a-coverage-group"></a>Vytvoření skupiny disponibility
1. Přejděte na Skupiny disponibility.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina disponibility.
4. Zadejte hodnotu do pole Název.
5. Zadejte hodnotu do pole Kalendář.
    * Vyberte kalendář, že který se používá v hlavním plánování k vytvoření návrhu doplnění pro položky v této skupině.  
6. Vyberte možnost v poli Kód disponibility.
    * Vyberte požadavek pro tento postup.  
7. V poli Ochranná doba disponibility (ve dnech) zadejte číslo 90.
    * Pro položky v této skupině použijte hlavní plánování k vytvoření návrhu doplnění pro až 90 dnů v budoucnosti.  
8. V poli Dny zpoždění zadejte číslo 1.
9. V poli Kladné dny zadejte číslo 1.
10. Rozbalte nebo sbalte oddíl Jiné.
11. V poli Rezerva příjmu přičtená k požadovanému datu zadejte číslo 1.
    * Pokud je například rezerva příjmu nastavena 1 den a řádek nákupní objednávky je naplánován na příjem dne 15. května, hlavní plánování vypočte upravené datum příjmu 16. května.  
12. V poli Rezerva výdeje odečtená od požadovaného data zadejte číslo 1.
    * Pokud je například pojistná doba nastavena na 1 den a řádek prodejní objednávky je naplánován na dodání 15. května, hlavní plánování vypočte upravené datum dodání 14. května.  
13. V poli Rezerva přidaná k době realizace položky zadejte číslo 1.
14. Klikněte na položku Uložit.

## <a name="create-a-new-product"></a>Vytvořit nový produkt
1. Přejděte na Uvolněné produkty.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Číslo produktu.
4. Do pole Název produktu zadejte hodnotu.
5. V poli Skupina modelů položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
12. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. Klikněte na tlačítko OK.

## <a name="setup-default-order-settings"></a>Nastavení výchozího nastavení objednávky
1. V podokně akcí klikněte na položku Plán.
2. Klikněte na Výchozí nastavení objednávky.
3. Do pole Nákupní pracoviště zadejte pracoviště, které chcete použít jako výchozí při vytvoření nákupní objednávky.
4. Do pole Skladové pracoviště zadejte site, kde je položka uložena.
5. Rozbalte nebo sbalte oddíl Zásoby.
6. Nastavte Násobek na hodnotu 10.
7. Nastavte Min. množství objednávky na 10.
8. Nastavte maximální. množství objednávky na 100.
9. Nastavte Standardní množství objednávky na 10.
10. Do pole Doba realizace nákupu zadejte číslo.
11. Zaškrtněte políčko Pracovní dny nebo jeho zaškrtnutí zrušte.
12. Klikněte na položku Uložit.
13. V poli Výchozí typ objednávky vyberte možnost Nákupní objednávka.
14. Klikněte na položku Uložit.
15. Zavřete stránku.
    * Zavřete stránku Výchozí nastavení objednávky.  

## <a name="add-an-item-to-a-coverage-group"></a>Přidání položky do skupiny disponibility
1. Rozbalte nebo sbalte oddíl Plán.
2. V poli Skupina disponibility kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. V seznamu vyhledejte skupiny disponibility, kterou jste vytvořili.
4. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="create-item-coverage-rules"></a>Vytvoření pravidel disponibility položky
1. V podokně akcí klikněte na položku Plán.
2. Klikněte na Disponibilita položky.
3. Klikněte na položku Nová.
4. Klikněte na záložku Obecné.
5. Zaškrtněte políčko v záhlaví Přepsat nastavení skupiny disponibility.
6. V poli Ochranná doba disponibility (ve dnech) zadejte číslo 60.
    * I když jsou položky ve skupině disponibility Požadavky plánované 90 dnů dopředu, tato položka bude plánovaná 60 dní dopředu.  
7. V poli Dny zpoždění zadejte číslo 2.
8. V poli Kladné dny zadejte číslo 2.
9. Klikněte na kartu Doba realizace.
10. Zaškrtněte políčko v záhlaví Nákup.
11. Do pole Čas nákupu zadejte hodnotu 5.
12. Klikněte na položku Uložit.

