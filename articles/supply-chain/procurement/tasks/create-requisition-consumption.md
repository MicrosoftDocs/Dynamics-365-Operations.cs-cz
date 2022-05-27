---
title: Vytvoření žádanky pro spotřebu
description: Toto téma popisuje postup vytváření žádosti.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5881e8a415ad37ff4bdb61b1043901c0b87ef743
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671116"
---
# <a name="create-a-requisition-for-consumption"></a>Vytvoření žádanky pro spotřebu

[!include [banner](../../includes/banner.md)]

Toto téma popisuje postup vytváření žádosti. Ukazuje různé způsoby, jak vyhledávat produkty v zásobovacím katalogu a jak přidat produkt, který není ve vašem katalogu. Před zahájením tohoto postupu je nutné mít nastavenou zásadu nákupu s výchozím typem žádanky Spotřeba. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Postup můžete provést pouze pomocí uživatelského profilu, který je nastavený jako pracovník. Tento úkol běžně provádí zaměstnanec. Role zabezpečení **Zaměstnanec** vám umožní provádět úkoly a pokud používáte data USMF, můžete se přihlásit jako **Alicia**.


## <a name="create-a-new-requisition"></a>Vytvoření nové žádanky
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní žádanky > Mnou připravené nákupní žádanky**.
2. Zvolte **Nové**.
3. V poli **Název** zadejte pro žádanku název.
4. Zadejte datum do pole **Požadované datum**. Ve výchozím nastavení je požadované datum a datum účtování zkopírováno na řádky nákupních žádanek. Ty lze měnit na úrovni řádku. Požadované datum představuje požadované datum dodávky.  
5. Zadejte datum do pole **Datum účtování**. Účetní datum je použité k záznamu účetní položky v hlavní knize a ověření dostupných rozpočtových prostředků.  
6. Vyberte **OK**.
7. V poli **Důvod** vyberte z rozevírací nabídky požadovanou možnost. Vybraná obchodní zdůvodnění se ve výchozím nastavení zobrazí na řádcích nákupní žádanky. Podle potřeby je však můžete změnit na úrovni řádku.  
8. Vyberte důvod.
9. V poli **Podrobnosti** zadejte popisnější odůvodnění žádanky.

## <a name="add-a-line-to-the-requisition"></a>Přidání řádku do žádanky
1. Vyberte **Přidat řádek**. Existují dva způsoby přidání řádků do nákupní žádanky. Pokud již znáte číslo produktu nebo již víte, že požadujete produkt, který se nenachází v katalogu produktů, přidejte řádek přímo pomocí možnosti **Přidat řádek**. Můžete také použít možnost **Přidat produkty** a pomocí vyhledávání a filtrování najít položky v katalogu produktů.    
2. Vyberte řádek, který jste právě vytvořili.
    - Žadatel je pracovník, který vyžaduje žádanku.   
    - Ve výchozím nastavení je osoba připravující žádanku pracovníkem, který odeslal požadavek. Musíte mít oprávnění k přípravě řádku žádanky jménem jiného pracovníka. Pokud takové oprávnění máte, v tomto vyhledávání se zobrazí tito ostatní pracovníci.  
3. Zadejte hodnotu do pole **Číslo zboží**. Položky, které můžete vybrat, jsou omezeny zásadami přístupu ke kategorii a zásobovacím katalogem pro kupující právnickou osobu.   
4. Zadejte číslo do pole **Množství**.

## <a name="add-more-products-to-the-requisition"></a>Přidání dalších produktů do žádanky
1. Vyberte **Přidat produkty**. Toto je možnost, kde lze vyhledávat produkty v katalogu produktů.    
2. V poli **Vyhledání uzlu kategorie zásobování** zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na **Zadat**. Zadejte například `comput`.  
3. Použijte zástupce **InvokeDefaultButton**.
4. Pomocí pole **Filtr** filtrujte seznam produktů ve vybrané kategorii.
5. Vyberte kartu produktu, který chcete do žádanky přidat.
6. Vyberte **Přidat na řádky**.
7. Zadejte číslo do pole **Množství**.
8. V poli **Vyhledání uzlu kategorie zásobování** zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na **Zadat**. V tomto příkladu zadejte `High` (zvýrazňovače).  
9. Použijte zástupce **InvokeDefaultButton**.
10. Vyberte **Přidat neuvedené produkty na řádky**, chcete-li přidat produkt neuvedený v zásobovacím katalogu.
11. Do pole **Název produktu** zadejte hodnotu.
12. Do pole **Jednotka** zadejte hodnotu.
13. Vyberte **OK**.
14. Do pole **Popis položky** zadejte popis produktu.
15. Zadejte číslo do pole **Množství**.
16. Zadejte číslo do pole **Jednotková cena**. Pokud znáte cenu pro určitého dodavatele (vybraného v poli Účet dodavatele), můžete cenu zadat.   
17. V poli **Účet dodavatele** otevřete rozevírací seznam pro výběr možnosti. Dodavatelé, kteří jsou k dispozici v tomto poli, závisí na zásadách nákupu a stavu dodavatele pro aktuální kategorii zásobování. Místo volby dodavatele v tomto poli můžete vybrat tlačítko **Navrhnout dodavatele**.    
18. Ze seznamu vyberte dodavatele, kterého chcete použít.
19. Zadejte hodnotu do pole **Externí číslo položky**. Toto je referenční číslo produktu, který dodavatel zná. Například se může jednat o čísla položky produktu ve vlastním katalogu dodavatele.  
20. Vyberte **OK**.

## <a name="distribute-amounts"></a>Distribuovat částky
1. Vyberte **Finance**.
2. Vyberte **Distribuované částky**. Tento proces ukazuje, jak rozdělit náklady pro první řádek mezi 2 účty. To lze také provést později, když je požadavek ve stavu kontroly.  
3. Vybere **Rozdělit** k vytvoření nového řádku distribuce.
4. V poli **Účet hlavní knihy** vyberte první nákladové středisko, kde má být provedena část nákladů.
5. Vyberte druhý řádek distribuce.
6. Do pole Účet hlavní knihy zadejte druhé nákladové středisko.
7. Vyberte **Distribuovat rovnoměrně**.
8. Zavřete stránku.

## <a name="view-line-details"></a>Zobrazit podrobnosti řádku
1. Přepněte rozšíření oddílu **Podrobnosti řádku**.

## <a name="submit-the-requisition"></a>Odeslání žádanky
1. Kliknutím na možnost **Workflow** otevřete dialogové okno.
2. Vyberte **Odeslat**.
3. Zavřete stránku.
4. Do pole **Komentář** zadejte poznámky pro schvalovatele žádanky.
5. Vyberte **Odeslat**.
6. Zavřete stránku.
7. Aktualizujte stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]