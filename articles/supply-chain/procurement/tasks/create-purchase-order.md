---
title: Vytvoření nákupní objednávky
description: Toto téma popisuje způsob ručního vytváření nákupní objednávky.
author: GalynaFedorova
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2fd627b9874b3e3f7aad71fb2970ddcc333a608
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677387"
---
# <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

[!include [banner](../../includes/banner.md)]

Toto téma popisuje způsob ručního vytváření nákupní objednávky. Nákupní objednávky jsou obvykle vytvářeny automaticky jako výsledek hlavního plánování, přímé dodávky a jiných procesů. Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup. Zde uvedený příklad lze použít v rámci dat z ukázkové společnosti USMF při použití hodnot, které jsou doporučeny v rámci poznámek pro různé kroky.


## <a name="create-the-purchase-order-header"></a>Vytvoření záhlaví nákupní objednávky
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**.
2. Zvolte **Nové**.
3. Vyberte účet dodavatele **US-101**. Pokud vyberete dodavatele, informace ze záznamu dodavatele, jako je například adresa, fakturační účet, dodací podmínky a režim, budou zkopírovány jako výchozí hodnoty do záhlaví objednávky. Tyto hodnoty lze kdykoli změnit.  
4. Rozbalte sekci **Obecné**.

    - Pole **Pracoviště** v kombinaci s polem **Sklad** určuje, kam je třeba opatřené zboží nebo služby odeslat. Výchozí dodací adresu je dané pracoviště. Obě pole lze vyplnit hodnotami nastavenými pro vybraného dodavatele, nebo je lze zadat ručně.  
    - Pole **Datum dodání** lze použít v případě, že získané zboží a služby je nutné doručit. Můžete zadat jedno datum dodání pro celou objednávku, ale můžete také jednotlivé řádky objednávky doplnit o jedinečná data dodání. Pokud zde uvedené datum dodání nemůže být pro určité výrobky nebo služby dodrženo z důvodu delší realizace, vytvoří se tyto řádky s pozdějším datem dodání, které budou vzniklou situaci brát v potaz.  

5. Rozbalte oddíl **Správa**. Pole **Nákupčí** slouží k určení toho, kdo objednávku podal. To může být vhodné pro sdílení s dodavatelem v případě, že je třeba danou osobu kontaktovat. Do pole může být hodnota přiřazena automaticky, pokud je aktuální uživatelský účet přiřazen ke jménu na stránce **Uživatelé**.  
6. Vyberte **OK**. Tím jste dokončili vytvoření záhlaví objednávky. Při práci s řádky nákupní objednávky se zobrazí pouze souhrnné informace ze záhlaví. Chcete-li zobrazit zbývající informace, zvolte **Záhlaví**.  

## <a name="add-a-purchase-order-line"></a>Přidání řádku nákupní objednávky
1. Vyberte **Řádek nákupní objednávky**.
2. Vyberte **Dimenze**. Produkty mohou existovat ve více variantách, které se liší podle dimenzí, jako je barva, velikost nebo styl. Produkty lze také nastavit pro použití dimenzí úložiště, jako je například pracoviště nebo sklad. Existují také volitelné sledovací dimenze, jako například dávka nebo sériová čísla. Chcete-li zvýšit efektivitu zadání objednávek, můžete přidat nejčastěji používaná pole dimenzí přímo do mřížky objednávky.  
3. Označte pole **Barva**. Volitelné: Označíte-li pole **Uložit nastavení**, vybrané dimenze se při příštím otevření stránky nákupní objednávku zobrazí také v mřížce řádků objednávky.  
4. Vyberte **OK**.
5. V poli **Číslo položky** zvolte **T0004**.

    - Řádky objednávky jsou vytvářeny pro produkty a služby stanovením čísla položky nebo výdajů, a to určením kategorie zásobování. 
    - Pole **Kategorie zásobování** slouží k přidávání řádků, kde jsou opatřené položky zaneseny do výdajů přímo, namísto přesměrování mezi zásoby. To znamená, že pokud je třeba zanést nákup do výdajů, lze to provést vytvořením řádku nákupní objednávky, který určuje kategorii zásobování, namísto vytvoření řádku s číslem položky. Položky lze také přiřadit ke kategorii zásobování. V takovém případě je kategorie zásobování zobrazena pouze informativně.  

6. V poli **Barva** zadejte nebo vyberte hodnotu. Do pole **Pracoviště** a **Sklad** se obvykle vyplní hodnoty ze záhlaví objednávky, ale pole je možné přepsat, pokud je třeba některé řádky doručit na různá místa.  
7. Zadejte číslo do pole **Množství**.

    - Určete množství, které se má nakoupit. V poli **Množství** bude automaticky vyplněno minimální množství objednávky pro produkt (je-li nastaven) nebo hodnota 1.  
    - V poli **Jednotka** vyberte měrnou jednotku pro objednané množství. Obvykle je jednotka automaticky uváděna z nákupní jednotky v rámci hlavních dat produktu. To však lze změnit.  
    - Pole **Cena jednotky** obvykle obsahuje hodnotu z nákupní smlouvy nebo obchodní smlouvy. Je možné změnit jednotkovou cenu na jednotlivých řádcích objednávky, například pokud je nasmlouvána jedinečná cena s dodavatelem.  
    - Pole **Sleva** obsahuje částku slevy za každou jednotku. Tato sleva proto snižuje jednotkovou cenu o výši slevy. Tato sleva je zpravidla dodávána automaticky z obchodních nebo nákupních smluv, ale je možné ji přepsat pro jednotlivé řádky v případě, že byla s dodavatelem vyjednána jedinečná sleva.  
    - Je možné zadat procento slevy, které odpovídajícím způsobem snižuje čistou částku pro řádek. Toto procento slevy je zpravidla dodáváno automaticky z obchodních nebo nákupních smluv, ale je možné je přepsat pro jednotlivé řádky v případě, že byla s dodavatelem vyjednána jedinečná procentuální sleva.  
    - Hodnotu v poli **Čistá částka** se počítá z dalších polí na řádku, včetně množství, jednotkové ceny, slevy a procenta slevy. Čistou částku lze změnit, ale poté pole **Jednotková cena**, **Sleva** a **Procento slevy** zůstanou nevyplněné a při zaúčtování k řádku bude zaúčtována částka přiměřená s ohledem na čistou částku. Pole **Čistá částka** se obvykle používá pouze pro zobrazení čisté částky na řádku.  

8. Rozbalte sekci **Podrobnosti řádku**.
9. Zvolte kartu **Doručení**. Jedinečné datum doručení, které lze přiřadit ke každému řádku objednávky. Datum pochází z pole v záhlaví nákupní objednávky, ale lze je změnit.  

## <a name="review-order-totals"></a>Kontrola součtů objednávky
1. Vyberte možnost **Součty**.

    - Pokud akci **Celkem** nevidíte, zvolte kartu **Nákupní objednávka** v podokně akcí.  
    - V tomto dialogovém jsou zobrazeny součty pro celou objednávku.  
    - Pole **Výběr** umožňuje změnit základ způsobu výpočtu součtů. Například můžete vybrat **Množství v příjemce produktu** a zobrazit tak celkové hodnoty, které se vztahují k množství produktů, které byly přijaty, nebo vybrat **Objednané množství** a zobrazit množství produktu, které byly objednány.  

2. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]