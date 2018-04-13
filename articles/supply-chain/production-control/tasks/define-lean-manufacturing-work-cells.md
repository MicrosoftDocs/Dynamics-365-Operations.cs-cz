--- 
title: "Definování pracovních buněk pro lean manufacturing"
description: "Pracovní buňka je konkrétní formulář skupin prostředků, které lze použít v aktivitách procesu lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f060f084baab055a51e390f488ca2553bd997b92
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-manufacturing-work-cells"></a>Definování pracovních buněk pro lean manufacturing

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Pracovní buňka je konkrétní formulář skupin prostředků, které lze použít v aktivitách procesu lean manufacturing. Pracovní buňky mají vstupní a výstupní skladová místa a definování kapacity založená na modelu výrobního toku. Další informace o základních konceptech pracovních buněk lean manufacturingu a výpočtů kapacity najdete v dokumentech white paper o Lean manufacturingu. Použitá ukázková data společnosti USMF k vytvoření tohoto postupu


## <a name="create-a-work-cell"></a>Vytvoření pracovní buňky 
1. Přejděte na nabídce Správa organizace > Zdroje > Skupiny prostředků.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina prostředků.
    * ID pracovní buňky je obvykle systematický kód a musí být pro právnickou osobu jedinečný.  
4. Zadejte nějakou hodnotu do pole Popis.
    * Popis obsahuje název nebo nadpis pracovní buňky.  
5. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Pracovní buňka se nachází v jednom konkrétním pracovišti. Vstup a výstup skladu a umístění je nutné umístit na tomto webu.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Výrobní jednotka klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte výrobní jednotku, které patří tato pracovní buňka.  
9. Zaškrtněte políčko Pracovní buňka.
    * K použití skupiny prostředků jako štíhlé pracovní buňky je nutné vybrat políčko pracovní buňka.  Všimněte si, že tuto vlastnost nelze změnit po vytvoření skupiny prostředků.  
10. V poli Vstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Klikněte na odkaz na vybraném řádku v seznamu.
    * Pro účetnictví a kontrolu materiálu je materiál umístěný v dílně obvykle přidělen do určitého virtuálního skladu. Nicméně, pokud chcete doplnit umístění pomocí skladové práce, doplnění musí být součástí skladu pasivních surovin.  
12. V poli Vstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Klikněte na odkaz na vybraném řádku v seznamu.
    * Všimněte si, že pro aktivitu procesu vstupní místo lze obecně přepsáním nebo pro konkrétní produkt nebo variantu produktu definováním aktivity výdeje, která je vložena do aktivity procesu. Vstupní místa pracovní buňky nelze řídit registrační značkou.  
14. V poli Výstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V několika výrobních tocích aktivity nebo řádcích výroby je toto často vstupním skladem následující pracovní buňky nebo prodejním či tranzitním skladem, kam produkty jsou obvykle převedeny po procesu výroby. Mějte na paměti při modelování procesů lean manufacturing, že přeprava je obvykle odpadní, jako vykazování přepravy.  
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. V poli Výstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Ve výrobním toku s více aktivitami zpracování je toto často vstupním umístěním následující pracovní buňky.  
18. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
19. Klikněte na odkaz na vybraném řádku v seznamu.
20. Rozbalte nebo sbalte oddíl Operace.
    * Aby bylo možné povolit výpočet nákladů a zpracování štíhlé kanbanové úlohy, musí být zadána kategorie operačního času.  
21. V poli Kategorie operačního času klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
22. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Operační čas nákladové kategorie se používá ve výpočtu standardních nákladů a zpětného účtování nákladů.  
23. Klikněte na odkaz na vybraném řádku v seznamu.
24. Rozbalte nebo sbalte oddíl Kalendáře.
25. Klepněte na možnost Přidat.
26. V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
27. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Obvykle pracovní buňky daného pracoviště používají stejný kalendář pracovní doby. Pokud pracovní buňky mohou mít jednotlivé pracovní doby, můžete potřebovat vytvořit konkrétní kalendář pracovní doby pro pracovní buňku. Nezapomeňte, že když je kalendář použitý pro štíhlou pracovní buňku, měl by mít definovanou standardní pracovní dobu související se standardní pracovní dobou pracovního dne.  
28. Klikněte na odkaz na vybraném řádku v seznamu.
29. Rozbalte nebo sbalte část Kapacita pracovní buňky.
30. Klepněte na možnost Přidat.
31. V poli Model výrobního toku klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
32. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Tento postup vyžaduje typ modelu výrobního toku Propustnost, aby se dalo zobrazit definici kapacity propustnosti.  
33. Klikněte na odkaz na vybraném řádku v seznamu.
34. V poli Období kapacity vyberte možnost.
    * Možnosti zahrnují:   Standardní pracovní den – kapacita je vyjádřena délkou standardního pracovního dne kalendáře pracovní doby pro pracovní buňku. Pro každý den skutečná pracovní doba se určuje na základě kalendáře, a na jeho základě se vypočítává platná dostupná kapacita.   Týden – umožňuje týdenní kapacitu. Podle skutečné pracovní doby není nutné provádět žádnou úpravu.   Měsíc – umožňuje měsíční kapacitu. Podle skutečné kapacity není nutné provádět žádnou úpravu.   Obvykle se používá standardní pracovní den pro denní období a týdenní kapacita se používá pro týdenní období kapacity.  
35. V poli Průměrné množství propustnosti zadejte číslo.
    * Všimněte si, že štíhlé operace v ideálním prostředí nejsou nikdy nastaveny na maximální možnou kapacitu. Namísto toho by vždy měla být kapacita definována pro operace, které jsou spouštěny za typických okolností.  
36. V poli Jednotka klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
37. Klikněte na odkaz na vybraném řádku v seznamu.
38. Vyřešit změny jednotky.

## <a name="add-a-financial-dimension"></a>Přidání finanční dimenze
1. Rozbalte nebo sbalte oddíl Finanční dimenze.
    * Všimněte si, že finanční dimenze určené ve výrobním tok přepisují finanční dimenzi dané pracovní buňky.    Finanční dimenze, které lze vybrat, závisejí na konfiguraci finančních dimenzí vašeho systému. Následující kroky odpovídají sadě dat ukázkové společnosti USMF. Při použití jiných dat tyto kroky nemusí platit.  
2. V poli Nákladové středisko kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Dimenze, které musí být ve štíhlých pracovních buňkách vybrány, závisí na implementaci finančních dimenzí v účetním modelu pro určitou právnickou osobu.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="save"></a>Uložit
1. Klikněte na položku Uložit.


