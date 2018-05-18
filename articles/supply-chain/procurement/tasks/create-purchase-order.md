--- 
title: "Vytvoření nákupní objednávky"
description: "Tato procedura popisuje způsob ručního vytváření nákupní objednávky."
author: FrankDahl
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob ručního vytváření nákupní objednávky. Nákupní objednávky jsou obvykle vytvářeny automaticky jako výsledek hlavního plánování, přímé dodávky a jiných procesů. Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup. Zde uvedený příklad lze použít v rámci dat z ukázkové společnosti USMF při použití hodnot, které jsou doporučeny v rámci poznámek pro různé kroky.


## <a name="create-the-purchase-order-header"></a>Vytvoření záhlaví nákupní objednávky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Vyberte účet dodavatele US-101.
    * Pokud vyberete dodavatele, informace ze záznamu dodavatele, jako je například adresa, fakturační účet, dodací podmínky a režim, budou zkopírovány jako výchozí hodnoty do záhlaví objednávky. Tyto hodnoty lze kdykoli změnit.  
4. Rozbalte sekci Obecné.
    * Pole Pracoviště v kombinaci s polem Sklad určuje, kam je třeba opatřené zboží nebo služby odeslat. Výchozí dodací adresu je dané pracoviště. Obě pole lze vyplnit hodnotami nastavenými pro vybraného dodavatele, nebo je lze zadat ručně.  
    * Pole Datum dodání lze použít v případě, že získané zboží a služby je nutné doručit. Můžete zadat jedno datum dodání pro celou objednávku, ale můžete také jednotlivé řádky objednávky doplnit o jedinečná data dodání. Pokud zde uvedené datum dodání nemůže být pro určité výrobky nebo služby dodrženo z důvodu delší realizace, vytvoří se tyto řádky s pozdějším datem dodání, které budou vzniklou situaci brát v potaz.  
5. Sbalte oddíl Obecné.
6. Rozbalte oddíl Správa.
    * Pole Nákupčí slouží k určení toho, kdo objednávku podal. To může být vhodné pro sdílení s dodavatelem v případě, že je třeba danou osobu kontaktovat. Do pole může být hodnota přiřazena automaticky, pokud je aktuální uživatelský účet přiřazen ke jménu na stránce Uživatelé.  
7. Sbalte oddíl Správa.
8. Klikněte na tlačítko OK.
    * Tím jste dokončili vytvoření záhlaví objednávky. Při práci s řádky nákupní objednávky se zobrazí pouze souhrnné informace ze záhlaví. Chcete-li zobrazit zbývající informace, klikněte na záhlaví.  

## <a name="add-a-purchase-order-line"></a>Přidání řádku nákupní objednávky
1. Klikněte na Řádek nákupní objednávky.
2. Klikněte na Dimenze.
    * Produkty mohou existovat ve více variantách, které se liší podle dimenzí, jako je barva, velikost nebo styl. Produkty lze také nastavit pro použití dimenzí úložiště, jako je například pracoviště nebo sklad. Existují také volitelné sledovací dimenze, jako například dávka nebo sériová čísla. Chcete-li zvýšit efektivitu zadání objednávek, můžete přidat nejčastěji používaná pole dimenzí přímo do mřížky objednávky.  
3. Označte pole Barva.
    * Volitelné: Označíte-li pole Uložit nastavení, vybrané dimenze se při příštím otevření stránky nákupní objednávku zobrazí také v mřížce řádků objednávky.  
4. Klikněte na tlačítko OK.
5. Do pole Číslo položky vyberte „T0004“.
    * Řádky objednávky jsou vytvářeny pro produkty a služby stanovením čísla položky nebo výdajů, a to určením kategorie zásobování.  
    * Pole Kategorie zásobování slouží k přidávání řádků, kde jsou opatřené položky zaneseny do výdajů přímo, namísto přesměrování mezi zásoby. To znamená, že pokud je třeba zanést nákup do výdajů, lze to provést vytvořením řádku nákupní objednávky, který určuje kategorii zásobování, namísto vytvoření řádku s číslem položky. Položky lze také přiřadit ke kategorii zásobování. V takovém případě je kategorie zásobování zobrazena pouze informativně.  
6. V poli Barva zadejte nebo vyberte hodnotu.
    * Do pole Pracoviště a Sklad se obvykle vyplní hodnoty ze záhlaví objednávky, ale pole je možné přepsat, pokud je třeba některé řádky doručit na různá místa.  
7. Zadejte číslo do pole Množství.
    * Určete množství, které se má nakoupit. V poli Množství bude automaticky vyplněno minimální množství objednávky pro produkt (je-li nastaven) nebo hodnota 1.  
    * V poli Jednotka vyberte měrnou jednotku pro objednané množství. Obvykle je jednotka automaticky uváděna z nákupní jednotky v rámci hlavních dat produktu. To však lze změnit.  
    * Pole Cena jednotky obvykle obsahuje hodnotu z nákupní smlouvy nebo obchodní smlouvy. Je možné změnit jednotkovou cenu na jednotlivých řádcích objednávky, například pokud je nasmlouvána jedinečná cena s dodavatelem.  
    * Pole Sleva obsahuje částku slevy za každou jednotku. Tato sleva proto snižuje jednotkovou cenu o výši slevy. Tato sleva je zpravidla dodávána automaticky z obchodních nebo nákupních smluv, ale je možné ji přepsat pro jednotlivé řádky v případě, že byla s dodavatelem vyjednána jedinečná sleva.  
    * Je možné zadat procento slevy, které odpovídajícím způsobem snižuje čistou částku pro řádek. Toto procento slevy je zpravidla dodáváno automaticky z obchodních nebo nákupních smluv, ale je možné je přepsat pro jednotlivé řádky v případě, že byla s dodavatelem vyjednána jedinečná procentuální sleva.  
    * Hodnotu v poli Čistá částka se počítá z dalších polí na řádku, včetně množství, jednotkové ceny, slevy a procenta slevy. Čistou částku lze změnit, ale poté pole Jednotková cena, Sleva a Procento slevy zůstanou nevyplněné a při zaúčtování k řádku bude zaúčtována částka přiměřená s ohledem na čistou částku. Pole Čistá částka se obvykle používá pouze pro zobrazení čisté částky na řádku.  
8. Rozbalte sekci Podrobnosti řádku.
9. Klikněte na záložku Dodání.
    * Jedinečné datum doručení, které lze přiřadit ke každému řádku objednávky. Datum pochází z pole v záhlaví nákupní objednávky, ale lze je změnit.  
10. Sbalte oddíl Podrobnosti řádku.

## <a name="review-order-totals"></a>Kontrola součtů objednávky
1. Klikněte na položku Součty.
    * Pokud akci Celkem nevidíte, klepněte na kartu Nákupní objednávky na panelu akcí.  
    * V tomto dialogovém jsou zobrazeny součty pro celou objednávku.  
    * Pole Výběr umožňuje změnit základ způsobu výpočtu součtů. Například můžete vybrat Množství v příjemce produktu a zobrazit tak celkové hodnoty, které se vztahují k množství produktů, které byly přijaty, nebo vybrat Objednané množství a zobrazit množství produktu, které byly objednány.  
2. Klikněte na tlačítko OK.


