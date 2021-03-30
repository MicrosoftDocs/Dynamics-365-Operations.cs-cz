---
title: Nastavení objednávek kvality
description: Tento postup popisuje povolení procesu řízení kvality, kde musí být příchozí zásoby okamžitě po registraci po doručení prohlédnuty.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351b2ce6b5678976fa8c46908c16dbadbbe23e97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244296"
---
# <a name="set-up-quality-orders"></a>Nastavení objednávek kvality

[!include [banner](../../includes/banner.md)]

Tento postup popisuje povolení procesu řízení kvality, kde musí být příchozí zásoby okamžitě po registraci po doručení prohlédnuty. Postup obvykle provádí správce kvality. Proces zahrnuje vytvoření skupiny kvality, definování položek, které budou testovány, a sestavení skupiny testů, které mají být provedeny u položek ve skupině kvality. Tohoto průvodce můžete spustit s ukázkovými daty společnosti USMF.


## <a name="enable-quality-management"></a>Povolení správy kvality
1. Přejděte na **Navigační podokno > Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.
2. Klikněte na kartu **Správa kvality**.
3. Volbu **Použít správu kvality** nastavte na hodnotu ‚Ano‘.
4. Klikněte na **Nastavení sestavy**. V USMF je nastavení sestavy pro správu kvality již definováno. Pokud k tomu nedošlo, přidejte zde nové řádky pro různé typy sestav a vyberte typ dokumentu, který má být použit pro každou sestavu.  
5. Zavřete stránku.
6. Zavřete stránku.

## <a name="create-a-test"></a>Vytvoření testu
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testy**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Test**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte ‚Možnost‘ v poli **Typ**. V tomto příkladu vyberete Možnost, což nám umožní přiřazení výsledků testu na základě předem definovaných hodnot.  
6. Klikněte na možnost **Uložit**.
7. Zavřete stránku.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Vytvoření proměnných testu pro určení způsobu zaznamenávání výsledků testů
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testovací proměnné**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Proměnná**.
4. Zadejte hodnotu do pole **Popis**.
5. Klikněte na možnost **Uložit**.
6. Klikněte na tlačítko **Výsledky**.
7. Klepněte na možnost **Nový**.
8. Zadejte hodnotu do pole **Výsledek**.
9. Zadejte hodnotu do pole **Popis**.
10. Vyberte volbu ‚Úspěch‘ v poli **Stav výsledku**.
11. Klikněte na možnost **Uložit**.
12. Klepněte na možnost **Nový**.
13. Zadejte hodnotu do pole **Výsledek**.
14. Zadejte hodnotu do pole **Popis**.
15. Klikněte na možnost **Uložit**.
16. Zavřete stránku.
17. Zavřete stránku.

## <a name="set-up-item-sampling"></a>Nastavení vzorkování zboží
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Vzorkování položky**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Vzorkování položky**.
4. Zadejte hodnotu do pole **Popis**.
5. Zadejte číslo do pole **Hodnota**. Tato hodnota se vztahuje k Určení množství, které je vybráno v přilehlém poli.  
6. Rozbalte nebo sbalte oddíl **Zpracování**.
7. Zaškrtněte políčko **Úplné blokování** nebo jeho zaškrtnutí zrušte. Pokud vyberete tuto možnost a test se nezdařil, je blokováno celé množství řádku šarže nebo zakázky. Pokud pole nevyberete, pouze položky v rámci objednávky kvality jsou blokovány.  
8. Klikněte na možnost **Uložit**.
9. Zavřete stránku.

> [!NOTE]
> Funkce *Správa kvality pro procesy skladu* poskytuje dodatečné možnosti vzorkování zboží. Přidá koncepci *rozsahu vzorkování položek* a možnost definovat plnou registrační značku jako specifikaci množství. Pokud jste tuto funkci povolili, další informace naleznete v tématu [Správa kvality pro procesy skladu](../quality-management-for-warehouses-processes.md).

## <a name="create-a-quality-group"></a>Vytvoření skupiny kvality
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Skupiny kvality**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Skupiny kvality**. Popisný název usnadňuje identifikaci toho, které druhy položek skupina obsahuje (kritéria vzorkování).  
4. Zadejte hodnotu do pole **Popis**.
5. Klikněte na možnost **Uložit**.
6. Klikněte na možnost **Přidat položky**.
7. Vyberte řádek **Číslo položky**. V tomto příkladu filtrování bude spuštěno podle čísla položky.  
8. Zadejte hodnotu do pole **Kritéria**. Pokud například zadáte T*, dojde k filtrování čísel položek pouze na ty, které začínají na písmeno T.  
9. Klikněte na tlačítko **OK**.
10. Klikněte na tlačítko **OK**.
11. Klikněte na **Skupiny kvality zboží**.
12. Zavřete stránku.
13. Zavřete stránku.

## <a name="create-a-test-group"></a>Vytvoření testovací skupiny
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testovací skupiny**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Testovací skupiny**. Udělte **Testovací skupině** název, který vám pomůže zapamatovat, jaké testy budou spuštěny, a se kterou skupinou kvality by měla být přidružena. Například pokud ji budete používat se skupinou kvality, která vybírá položky začínající na „T“, mohli byste ji nazvat „Testy položek T“.  
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Vzorkování položky** vyberte řádek vzorkování položky, který jste vytvořili dříve.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na tlačítko **Přidat**.
8. V poli **Pořadové číslo** zadejte číslo.
9. V poli **Test** vyberte test vytvořený dříve.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
11. Klepněte na kartu **Test**.
12. V poli **Proměnná** vyberte proměnnou testu vytvořenou dříve
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. V poli **Výchozí výsledek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. Klikněte na možnost **Uložit**.
17. Zavřete stránku.

## <a name="define-when-quality-orders-will-be-created"></a>Určení toho, kdy budou vytvořeny objednávky kvality
1. Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Přiřazení kvality**.
2. Klepněte na možnost **Nový**.
3. Vyberte volbu v poli **Typ odkazu**.
4. V poli **Kód položky** vyberte Skupina. V tomto příkladu nyní vybereme „Skupina“ a použijeme dříve vytvořenou skupinu kvality. Můžete zde také nastavte možnost "Tabulka" a určit tak položky ručně, nebo vybrat "Vše" a přidat všechny položky do objednávky kvality.  
5. V poli **Položka** vyberte skupinu kvality, kterou jste vytvořili dříve. Možnosti dostupné v poli Položka závisí na nastavení v poli Kód položky.  
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Rozbalte nebo sbalte oddíl Zpracování.
8. Vyberte možnost v poli **Typ události**. Toto je událost, která spustí test. Možnosti zde dostupné závisí na procesu, který jste vybrali v poli Typu odkazu.  
9. Vyberte volbu v poli **Spuštění**.
10. Rozbalte nebo sbalte oddíl **Proces objednávky kvality**.
11. V poli **Blokování události** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. Toto pole zobrazí seznam procesů, které je možné blokovat, pokud je objednávka kvality stále otevřená. Možnosti závisí na vybrané možnosti v poli Typ události.  
12. Klikněte na odkaz na vybraném řádku v seznamu. To závisí na předchozích vybraných hodnotách. Určete, zda následující procesy musí být blokovány, zatímco jsou otevřené objednávky kvality připojeny k řádku zdrojového dokumentu.  
13. Rozbalte nebo sbalte oddíl **Specifikace**.
14. V poli **Testovací skupina** vyberte skupinu testu vytvořenou dříve.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
16. Klikněte na možnost **Uložit**.
17. Zavřete stránku.

> [!NOTE]
> Funkce *Správa kvality pro skladové procesy* poskytuje dodatečné možnosti pro nastavení přidružení kvality. Přidá novou podmínku (**Použitelný typ skladu**) a nové nastavení (**Zásady zpracování kvality**). Pokud jste tuto funkci povolili, další informace naleznete v tématu [Správa kvality pro procesy skladu](../quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]