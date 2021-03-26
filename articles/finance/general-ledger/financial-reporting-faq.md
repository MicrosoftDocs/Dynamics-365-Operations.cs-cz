---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249294"
---
# <a name="financial-reporting-faq"></a>Nejčastější dotazy k finančnímu výkaznictví 

Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Jak omezím přístup k sestavě pomocí zabezpečení stromu?

Scénář: Ukázková společnost USMF má sestavu rozvahy, která není určena všem uživatelům finančního výkaznictví v D365. Řešení: Pomocí zabezpečení stromu můžete omezit přístup některých uživatelů k sestavě. 

1.  Přihlášení do návrháře finančních sestav

2.  Vytvořte novou definici stromu (Soubor | Nový | Definice stromu). a.    Ve sloupci **Zabezpečení jednotky** poklepejte na řádek **Souhrn**.
  i.    Klikněte na možnost Uživatelé a skupiny.  
          1.    Vyberte uživatele nebo skupinu, která má mít přístup k této sestavě. 
          
[![obrazovka uživatele](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![obrazovka zabezpečení](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klikněte na tlačítko **Uložit**.
  
[![tlačítko uložit](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Do definice sestavy přidejte novou definici stromu.

[![formulář definice stromu](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  V definici stromu klikněte na Nastavení a v části „Výběr organizační jednotky“ zaškrtněte „Zahrnout všechny jednotky“.

[![formulář pro výběr organizační jednotky](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Před:** [![před screenshotem](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Po:** [![po screenshotu](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Poznámka: Výše uvedená zpráva se zobrazila, protože po použití zabezpečení jednotky nemá váš uživatel přístup k této sestavě.



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Jak zjistím, které účty neodpovídají mým zůstatkům v D365?

Pokud sestava v D365 neodpovídá vašim očekáváním, zde je několik kroků, kterými můžete identifikovat tyto účty a odchylky. 

### <a name="in-financial-reporter-report-designer"></a>V návrháři finančních sestav:

1.  Vytvořte novou definici řádků. a.    Klikněte na položku Upravit | Vložit řádky z dimenzí. i.  Vyberte Hlavní účet [![Výběr hlavní obrazovky](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Klikněte na tlačítko OK. b.    Uložte definici řádku.

2.  Vytvořte novou definici sloupce.     [![Vytvoření nové definice sloupce](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Vytvořte novou definici sestavy. a.    Klikněte na Nastavení a zrušte zaškrtnutí. [![Formulář Nastavení](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Vygenerujte sestavu. 

5.  Exportujte sestavu do aplikace Excel.

### <a name="in-d365"></a>V D365: 
1.  Klikněte na položky Hlavní kniha | Dotazy a sestavy | Předvaha. a.    Parametry: i.  Od data: Začátek fiskálního roku. ii. Do data: Datum, pro které jste vygenerovali sestavu. iii.    Sada finančních dimenzí nastavená jako „Sada hlavního účtu“. [![Formulář hlavního účtu](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Klikněte na tlačítko Vypočítat.

2.  Exportujte sestavu do aplikace Excel.

Nyní byste měli být schopni zkopírovat data ze sestavy finančního výkaznictví Excel a do sestavy předvahy D365 a porovnat sloupce „Konečný zůstatek“.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]