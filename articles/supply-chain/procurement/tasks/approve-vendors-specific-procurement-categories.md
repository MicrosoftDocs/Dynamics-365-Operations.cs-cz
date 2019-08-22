---
title: Schválení dodavatelů pro konkrétní kategorie zásobování
description: Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836329"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Schválení dodavatelů pro konkrétní kategorie zásobování

[!include [task guide banner](../../includes/task-guide-banner.md)]

Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny. Tento postup popisuje, jak určit, že je dodavatel schválený nebo upřednostňovaný pro specifickou kategorii zásobování. Tento úkol by obvykle prováděl zásobovací pracovník. Tento postup můžete projít v ukázkových datech společnosti USMF.

1. Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.
2. Vyberte dodavatele, kterého chcete nastavit jako schváleného nebo upřednostňovaného dodavatele pro kategorii.
3. V podokně akcí klikněte na položku Obecné.
4. Klikněte na Kategorie.
5. Klikněte na Přidat kategorii.
6. V poli Kategorie zaškrtněte KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ.
7. V poli Stav kategorie dodavatele vyberte „Upřednostňované“.
    * Je možné zadat více než jednoho upřednostněného dodavatele pro kategorii.  
8. Klikněte na položku Uložit.
9. Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.
10. Ve stromovém zobrazení vyberte “KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI\KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ“.
11. Rozbalte sekci Dodavatelé.
    * Zkontrolujte, zda se vámi vybraný dodavatel zobrazí jako upřednostněný dodavatel pro kategorii Kancelářské a stolní příslušenství. Pokud tento postup používáte jako průvodce úkolem, může být nutné kliknutím na tlačítko Odemknout umožnit procházení seznamem dodavatelů.  Také je možné přidat upřednostňované a schválené dodavatele na této stránce.  
12. Ve stromu rozbalte KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ.
13. Ve stromu vyberte Nůžky.
14. Vyberte Ne v poli Zdědit dodavatele z nadřazené kategorie:.
15. Vyberte Ano v poli Zdědit dodavatele z nadřazené kategorie:.

