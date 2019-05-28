---
title: Konfigurace zpracování vlny
description: Tento průvodce popisuje, jak nastavit kritéria určující práci, která vznikne pro sklad při zpracování vlny, a zda jsou vlny zpracovány ručně nebo automaticky.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399146d35388a0151abb23e57bc36ec0173be928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571879"
---
# <a name="configure-wave-processing"></a>Konfigurace zpracování vlny

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce popisuje, jak nastavit kritéria určující práci, která vznikne pro sklad při zpracování vlny, a zda jsou vlny zpracovány ručně nebo automaticky. Podle potřeby určete kritéria nastavením šablon vlny a dotazů, které odpovídají vlně ve vydaných řádcích u prodejní objednávky, výrobní nebo kanbanové zakázce. Zpracování vlny se používá ve skladech, které používají funkce v modulu řízení skladu, nikoli ty, které používají funkce v modulu Řízení zásob. Tento postup můžete projít v ukázkových datech společnosti USMF.

1. Přejděte do nabídky Řízení skladu > Nastavení > Vlny > Šablony vlny.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název šablony vlny.
    * Během nastavení šablony vlny zadáváte pořadí, ve kterém budou šablony párovány s uvolněnými řádky na prodejních objednávkách, výrobních zakázkách nebo kanbanech. Když dojde k uvolnění řádku do skladu nebo do výroby, použije se první šablona vlny, pro kterou se splňují kritéria. Doporučujeme proto umístit šablony s nejkonkrétnějšími kritérii do horní části seznamu. Čím širší kritéria, tím pravděpodobněji řádek splní kritéria, a tím větší šance, že budou řádky přiřazeny k chybné vlně.  
4. Zadejte hodnotu do pole Popis šablony vlny.
5. V poli Lokalita zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat pracoviště 2.  
6. V poli Sklad zadejte nebo vyberte hodnotu.
    * Pokud používáte USMF, můžete vybrat sklad 24.  
7. V poli Automatizovat vytvoření vlny nastavte hodnotu Ano.
    * Vyberte tuto možnost, chcete-li automaticky vytvořit vlnu při vydání prodejní objednávky, výrobní zakázky nebo kanbanu do skladu.  
8. Nastavte možnost Zpracovat vlnu při uvolnění do skladu na Ano. 
    * Vyberte tuto možnost, chcete-li automaticky zpracovat vlnu a vytvořit práci při vydání řádku do skladu.  
9. Nastavte možnost Automatizovat uvolnění vlny na hodnotu Ano. 
    * Chcete-li automaticky uvolnit vlnu, vyberte tuto možnost. Výdej je vytvořen a je k dispozici pro mobilního zařízení.  
10. Nastavte možnost Přiřadit k otevřeným vlnám na Ano. 
    * Řádky jsou přiřazeny k vlně podle filtru dotazu pro šablonu vlny.  
11. Nastavte možnost Automaticky zpracovat vlnu při dosažení prahové hodnoty na Ano. 
    * Tuto možnost vyberte, chcete-li automaticky zpracovat vlnu, pokud její hodnoty dosáhnou prahové hodnoty pro hmotnost, dodávku a řádky uvedené ve skupině polí Prahové hodnoty vlny. Tato možnost je k dispozici jen tehdy, je-li v poli Typ šablony vlny vybrána možnost Expedice.  
12. Nastavte možnost Automatizovat uvolnění práce doplnění na hodnotu Ano. 
    * Výběrem této možnosti můžete vytvořit doplnění podle poptávky a automaticky je vydat. Musíte přidat metodu doplnění vlny do šablony vlny a vytvořit šablonu doplnění typu Poptávka vlny.  
13. Rozbalte sekci Způsoby.
    * Metody šablony vlny umožňují kontrolovat pořadí aktivit, skrze které každá vlna prochází během zpracování. Například můžete mít k dispozici metodu pro doplnění vlny. Při přidání metody se automaticky uvede v odpovídajícím umístění v pořadí kroků. Pokud nastavíte možnost Automatizovat uvolnění práce doplnění na hodnotu Ano, je třeba přidat metodu doplnění.  
    * Atributy vlny fungují jako filtry pro omezení druhu položek, které mohou používat vlny. Například můžete určit skupinu položek.  
14. Klikněte na položku Uložit.
15. Zavřete stránku.
16. Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.
17. Rozbalte část Zpracování vlny.
18. V poli Skupina dávky zpracování vlny zadejte nebo vyberte požadovanou hodnotu.
19. Nastavte Zpracovat vlny v dávce na hodnotu Ano.
20. V poli Čekat na uzamčení (ms) zadejte číslo.
    * Zadejte čas v milisekundách, po který se bude v rámci kroku přidělení čekat na systémové prostředky, které jsou uzamčený v dalším kroku přidělení. Při překročení tohoto času nebude vlna zpracována a zobrazí se chybová zpráva.  
21. Klikněte na položku Uložit.
22. Zavřete stránku.
23. Přejděte na Řízení výroby > Nastavení > Parametry modulu Řízení výroby.
24. V poli Uvolnit do skladu vyberte požadovanou možnost.
    * V případě prodejních objednávek a zakázek kanbanu je třeba vyhradit zásoby před vydáním objednávky do skladu. V opačném případě položky nebo řádky přidělení nelze zpracovat ve vlně. Pro výrobní zakázky můžete také využít možnost Povolit částečnou rezervaci. Například je to užitečné v případě, kdy vlastníte materiály potřebné k zahájení výroby, a můžete počkat, než budou pro dokončení procesu k dispozici další materiály. Pokud vyberete tuto možnost, je nutné ručně opakovat proces vydání do skladu, jakmile budou k dispozici další materiály.  
25. Zavřete stránku.

