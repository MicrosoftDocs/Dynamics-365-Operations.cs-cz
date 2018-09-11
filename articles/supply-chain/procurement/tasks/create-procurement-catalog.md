--- 
title: "Vytvoření zásobovacího katalogu"
description: "Tento postup popisuje způsob vytváření zásobovacího katalogu."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Vytvoření zásobovacího katalogu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob vytváření zásobovacího katalogu. Tento úkol by obvykle prováděl zásobovací pracovník. Zjistíte také, jak mohou zaměstnanci používat katalog při vytváření požadavku. Před vytvořením katalogu musí existovat ve vašem systému hierarchie kategorie zásobování. Hierarchii zdědí nový katalog spolu se všemi produkty, které jsou v hierarchii. Tento postup lze použít u ukázkových dat společnosti USMF, kde je k dispozici hierarchie kategorie zásobování společně s příklady použitými v krocích postupu.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Ujistěte se, že existuje hierarchie kategorie zásobování
1. Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.
    * U společnosti s demonstračními daty USMF je k dispozici hierarchie kategorie zásobování a produkty byly přidány do kategorie Kancelářské počítače. Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné kategorii procházet. Pokud hierarchii není k dispozici, vytvoříte ji klepnutím na možnost Nový. To je možné pouze jednou.  
2. Zavřete stránku.

## <a name="create-a-catalog"></a>Vytvoření katalogu
1. Přejděte do nabídky Zásobování a zdroje > Katalogy > Katalogy zásobování.
2. Kliknutím na možnost Nový zásobovací katalog otevřete dialogové okno.
3. Zadejte hodnotu do pole Název.
4. Klepněte na tlačítko OK.
5. Ve stromovém zobrazení rozbalte KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI.
6. Ve stromu rozbalte KANCELÁŘSKÉ POČÍTAČE.
7. Ve stromu vyberte Počítače.
    * V seznamu jsou zobrazeny produkty z kategorie zásobování. Pokud chcete přidat produkt do kategorie, je nutné to provést na stránce Hierarchie kategorií zásobování nebo Podrobnosti o zboží.  
    * Výchozí typ aktualizace určuje, zda jsou nové produkty přidané do hierarchie kategorie zásobování okamžitě viditelné v katalogu. Pokud je typ aktualizace nastaven na Dynamický, změny se projeví okamžitě. Pokud je typem aktualizace Statický, nové produkty jsou viditelné pouze uživatelům, kteří používají katalog po jeho opětovném publikování. Akce Publikovat je k dispozici v podokně Akce v horní části stránky. Pokud jsou produkty odebrány z hierarchie kategorie zásobování, změny se projeví okamžitě bez ohledu na hodnotu v poli Výchozí typ aktualizace.  
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Klikněte na Skrýt.
10. V podokně akcí klikněte na možnost Navigace v kategorii.
11. Klikněte na Zakázat.
12. V podokně akcí klikněte na možnost Navigace v kategorii.
13. Klikněte na tlačítko Povolit.
14. Klikněte na Aktivovat katalog.
15. Zavřete stránku.

## <a name="make-the-catalog-visible"></a>Zviditelnění katalogu
1. Přejděte na Zásobování a zdroje > Nastavení > Zásady > Zásady nákupu.
2. Vyberte USMF – zásady zásobování.
    * Je třeba vybrat zásady nákupu pro právnickou osobu, u které je pracovník propojený s profilem uživatele oprávněn objednávat produkty. V rámci ukázkových dat USMF je Administrátor je propojen s pracovníkem se jménem Julia Funderburk, která standardně objednává produkty v USMF.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Výběr katalog, který jste právě vytvořili.
5. Klikněte na tlačítko OK.
6. Zavřete stránku.
7. Zavřete stránku.

## <a name="use-the-catalog"></a>Použití katalogu
1. Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Všechny nákupní žádanky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Klikněte na tlačítko OK.
5. Klikněte na možnost Přidat produkty.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro filtrování produktů můžete použít hierarchii kategorií vlevo nebo filtr v horní části seznamu.  
7. Klikněte na možnost Přidat na řádky.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Klikněte na možnost Přidat na řádky.
10. Klikněte na tlačítko OK.


