---
title: Vytvoření zásobovacího katalogu
description: Toto téma vysvětluje postup při vytváření zásobovacího katalogu.
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812391"
---
# <a name="create-a-procurement-catalog"></a>Vytvoření zásobovacího katalogu

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje postup při vytváření zásobovacího katalogu. Tento úkol by obvykle prováděl zásobovací pracovník. Zjistíte také, jak mohou zaměstnanci používat katalog při vytváření požadavku. Před vytvořením katalogu musí existovat ve vašem systému hierarchie kategorie zásobování. Hierarchii zdědí nový katalog spolu se všemi produkty, které jsou v hierarchii. Tento postup lze použít u ukázkových dat společnosti USMF, kde je k dispozici hierarchie kategorie zásobování společně s příklady použitými v krocích postupu.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Ujistěte se, že existuje hierarchie kategorie zásobování
1. Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > Kategorie zásobování**. U společnosti s demonstračními daty USMF je k dispozici hierarchie kategorie zásobování a produkty byly přidány do kategorie **Kancelářské počítače**. Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné kategorii procházet. Pokud hierarchii není k dispozici, vytvoříte ji klepnutím na možnost **Nový**. To je možné pouze jednou.  
2. Zavřete stránku.

## <a name="create-a-catalog"></a>Vytvoření katalogu
1. Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > > Katalogy > Katalogy zásobování**.
2. Výběrem možnosti **Nový zásobovací katalog** otevřete dialogové okno pro přetažení.
3. Zadejte hodnotu do pole **Název**.
4. Vyberte **OK**.
5. Ve stromovém zobrazení rozbalte **KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI**.
6. Ve stromu rozbalte **KANCELÁŘSKÉ POČÍTAČE**.
7. Ve stromu vyberte **Počítače**.

  - V seznamu jsou zobrazeny produkty z kategorie zásobování. Pokud chcete přidat produkt do kategorie, je nutné to provést na stránce **Hierarchie kategorií zásobování** nebo **Podrobnosti o zboží**.  
  - **Výchozí** typ aktualizace určuje, zda jsou nové produkty přidané do hierarchie kategorie zásobování okamžitě viditelné v katalogu. Pokud je typ aktualizace nastaven na **Dynamický**, změny se projeví okamžitě. Pokud je typem aktualizace **Statický**, nové produkty jsou viditelné pouze uživatelům, kteří používají katalog po jeho opětovném publikování. Akce **Publikovat** je k dispozici v podokně Akce v horní části stránky. Pokud jsou produkty odebrány z hierarchie kategorie zásobování, změny se projeví okamžitě bez ohledu na hodnotu v poli **Výchozí** typ aktualizace.  

8. V podokně akcí vyberte **Navigace v kategorii** a ujistěte se, že je vybrána možnost **Povolit**.
9. Vyberte **Aktivovat katalog**.
10. Zavřete stránku.

## <a name="make-the-catalog-visible"></a>Zviditelnění katalogu
1. Přejděte na **navigační podokno > Moduly > Zásobování a nákup > Nastavení > Zásady > Zásady nákupu**.
2. Vyberte **USMF – zásady zásobování**. Je třeba vybrat zásady nákupu pro právnickou osobu, u které je pracovník propojený s profilem uživatele oprávněn objednávat produkty. V rámci ukázkových dat USMF je Administrátor je propojen s pracovníkem se jménem **Julia Funderburk**, která standardně objednává produkty v USMF.  
3. Výběr katalog, který jste právě vytvořili.
4. Vyberte **OK**.

## <a name="use-the-catalog"></a>Použití katalogu
1. Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > Nákupní žádanky > Všechny nákupní žádanky**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název**.
4. Vyberte **OK**.
5. Vyberte **Přidat produkty**.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Pro filtrování produktů můžete použít hierarchii kategorií vlevo nebo filtr v horní části seznamu.  
7. Vyberte **Přidat na řádky**.
8. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]