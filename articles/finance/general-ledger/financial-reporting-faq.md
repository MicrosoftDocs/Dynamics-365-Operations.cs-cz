---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923018"
---
# <a name="financial-reporting-faq"></a>Nejčastější dotazy k finančnímu výkaznictví 

Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Jak omezím přístup k sestavě pomocí zabezpečení stromu?

Následující příklad ukazuje, jak omezit přístup k sestavě pomocí zabezpečení stromu.

Ukázková společnost USMF má sestavu rozvahy, ke které by neměli mít přístup všichni uživatelé finančního výkaznictví. Pro omezení přístupu můžete pomocí zabezpečení stromu omezit přístup některých uživatelů k sestavě. Chcete-li omezit přístup, postupujte takto: 

1. Přihlaste se do aplikace Financial Reporter Report Designer.
2. Vytvořte novou definici stromu. Přejděte na **Soubor > Nový > Definice stromu**.
3. Ve sloupci **Zabezpečení jednotky** poklepejte na řádek **Souhrn**.
4. Zvolte **Uživatelé a skupiny**.  
5. Vyberte uživatele nebo skupiny, které mají mít přístup k této sestavě. 
6. Zvolte **Uložit**.
7. V definici sestavy přidejte svou novou definici stromu.
8. V definici stromu vyberte **Nastavení**. V možnosti **Výběr organizační jednotky** vyberte **Zahrnout všechny jednotky**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Jak zjistím, které účty neodpovídají mým zůstatkům?

Pokud máte sestavu, který nemá odpovídající zůstatky, je zde několik kroků, které můžete podniknout k identifikaci každého z účtů a odchylek. 

**Financial Reporter Report Designer**
1. V aplikaci Financial Reporter Report Designer vytvořte novou definici řádku. 
2. Zvolte **Upravit > Vložit řádky z dimenzí**.
3. Vyberte **Hlavní účet**.  
4. Vyberte **OK**.
5. Uložte definici řádku.
6. Vytvoření nové definice sloupce
7. Vytvořte novou definici sestavy.
8. Vyberte **Nastavení** a zrušte označení této možnosti.  
9. Vygenerujte sestavu. 
10. Exportujte sestavu do Microsoft Excel.

**Dynamics 365 Finance** 
1. V Dynamics 365 Finance, přejděte na **Hlavní kniha > Dotazy a sestavy > Předvaha**.
2. Nastavte následující parametry:
   - **Od data** - Zadejte začátek fiskálního roku.
   - **Do data** - Zadejte datum, pro které generujete sestavu.
   - **Finanční dimenze** - Nastavte toto pole na **Hlavní účet nastaven**.
 3. Vyberte **Vypočítat**.
 4. Exportujte sestavu do Microsoft Excel.

Nyní byste měli být schopni zkopírovat data ze sestavy finančního výkaznictví v Excelu a do sestavy předvahy a porovnat sloupce **Konečný zůstatek**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]