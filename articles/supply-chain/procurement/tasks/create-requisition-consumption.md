--- 
title: "Vytvoření žádanky pro spotřebu"
description: "Tato procedura vás provede procesem vytvoření žádanky."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d8ca4e7eedea140f32e264c205b243027a06d03
ms.openlocfilehash: d1ea95d0bc283297fcedaee730e1829850f07998
ms.contentlocale: cs-cz
ms.lasthandoff: 11/20/2017

---
# <a name="create-a-requisition-for-consumption"></a>Vytvoření žádanky pro spotřebu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede procesem vytvoření žádanky. Ukazuje různé způsoby, jak vyhledávat produkty v zásobovacím katalogu a jak přidat produkt, který není ve vašem katalogu. Před zahájením tohoto postupu je nutné mít nastavenou zásadu nákupu s výchozím typem žádanky Spotřeba. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Postup můžete provést pouze pomocí uživatelského profilu, který je nastavený jako pracovník.  Tento úkol běžně provádí zaměstnanec. Role zabezpečení zaměstnance vám umožní provádět úkoly a pokud používáte data USMF, můžete se přihlásit jako Alicia.


## <a name="create-a-new-requisition"></a>Vytvoření nové žádanky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Nákupní žádanky připravené mnou.
2. Klikněte na položku Nová.
3. V poli Název zadejte pro žádanku název.
4. Zadejte datum do pole Požadované datum.
    * Ve výchozím nastavení je požadované datum a datum účtování zkopírováno na řádky nákupních žádanek. Ty lze měnit na úrovni řádku. Požadované datum představuje požadované datum dodávky.  
5. Zadejte datum do pole Datum účtování.
    * Účetní datum je použité k záznamu účetní položky v hlavní knize a ověření dostupných rozpočtových prostředků.  
6. Klikněte na tlačítko OK.
7. V poli Důvod kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vybraná obchodní zdůvodnění se ve výchozím nastavení zobrazí na řádcích nákupní žádanky. Podle potřeby je však můžete změnit na úrovni řádku.    
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Volba důvodu
10. V poli Podrobnosti zadejte popisnější odůvodnění žádanky.

## <a name="add-a-line-to-the-requisition"></a>Přidání řádku do žádanky
1. Klikněte na položku Přidat řádek.
    * Existují dva způsoby přidání řádků do nákupní žádanky. Pokud již znáte číslo produktu nebo již víte, že požadujete produkt, který se nenachází v katalogu produktů, přidejte řádek přímo pomocí možnosti „Přidat řádek“. Můžete také použít možnost „Přidat produkty“ a pomocí vyhledávání a filtrování najít položky v katalogu produktů.    
2. Klikněte na řádek, který jste právě vytvořili.
    * Žadatel je pracovník, který vyžaduje žádanku.   
    * Ve výchozím nastavení je osoba připravující žádanku pracovníkem, který odeslal požadavek. Musíte mít oprávnění k přípravě řádku žádanky jménem jiného pracovníka. Pokud takové oprávnění máte, v tomto vyhledávání se zobrazí tito ostatní pracovníci.  
3. Zadejte hodnotu do pole Číslo zboží.
    * Položky, které můžete vybrat, jsou omezeny zásadami přístupu ke kategorii a zásobovacím katalogem pro kupující právnickou osobu.   
4. Zadejte číslo do pole Množství.

## <a name="add-more-products-to-the-requisition"></a>Přidání dalších produktů do žádanky
1. Klikněte na možnost Přidat produkty.
    * Toto je možnost, kde lze vyhledávat produkty v katalogu produktů.    
2. V poli Vyhledání uzlu kategorie zásobování zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na Zadat.
    * Zadejte například počít.  
3. Použijte zástupce InvokeDefaultButton.
4. Pomocí filtru filtrujte seznam produktů ve vybrané kategorii.
5. Vyberte kartu produktu, který chcete do žádanky přidat.
6. Klikněte na možnost Přidat na řádky.
7. Zadejte číslo do pole Množství.
8. V poli Vyhledání uzlu kategorie zásobování zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na Zadat.
    * Zadejte například zvýraz (zvýrazňovače).  
9. Použijte zástupce InvokeDefaultButton.
10. Klikněte na možnost Přidat neuvedené produkty na řádky, chcete-li přidat produkt neuvedený v zásobovacím katalogu.
11. Do pole Název produktu zadejte hodnotu.
12. Zadejte hodnotu do pole Jednotka.
13. Klepněte na tlačítko OK.
14. Do pole Popis položky zadejte popis produktu.
15. Zadejte číslo do pole Množství.
16. Zadejte číslo do pole Jednotková cena.
    * Pokud víte cenu pro určitého dodavatele (vybraného v poli Účet dodavatele), můžete cenu zadat.   
17. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Dodavatelé, kteří jsou k dispozici v tomto poli, závisí na zásadách nákupu a stavu dodavatele pro aktuální kategorii zásobování. Místo volby dodavatele v tomto poli můžete kliknout na tlačítko Navrhnout dodavatele.    
18. Ze seznamu vyberte dodavatele, kterého chcete použít.
19. Zadejte hodnotu do pole Externí číslo položky.
    * Toto je referenční číslo produktu, který dodavatel zná. Například se může jednat o čísla položky produktu ve vlastním katalogu dodavatele.  
20. Klikněte na tlačítko OK.

## <a name="distribute-amounts"></a>Distribuovat částky
1. Klepněte na tlačítko Finanční údaje.
2. Klikněte na možnost Distribuovat částky.
    * Tento proces ukazuje, jak rozdělit náklady pro první řádek mezi 2 účty. To lze také provést později, když je požadavek ve stavu kontroly.  
3. Kliknutím na Rozdělit vytvořte nový řádek distribuce.
4. V poli Účet hlavní knihy vyberte první nákladové středisko, kde má být provedena část nákladů.
5. Vyberte druhý řádek distribuce.
6. Do pole Účet hlavní knihy zadejte druhé nákladové středisko.
7. Klikněte na možnost Distribuovat rovnoměrně.
8. Zavřete stránku.

## <a name="view-line-details"></a>Zobrazit podrobnosti řádku
1. Přepněte rozšíření oddílu Podrobnosti řádku.

## <a name="submit-the-requisition"></a>Odeslání žádanky
1. Kliknutím na možnost Workflow otevřete dialogové okno.
2. Klepněte na tlačítko Odeslat.
3. Zavřete stránku.
4. Do pole Komentář zadejte poznámky pro schvalovatele žádanky.
5. Klepněte na tlačítko Odeslat.
6. Zavřete stránku.
7. Aktualizujte stránku.


