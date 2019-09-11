---
title: Schválení dodavatelů pro konkrétní kategorie zásobování
description: V tomto tématu je vysvětleno, jak schválit dodavatele pro určité kategorie zásobování v aplikaci Dynamics 365 for Finance and Operations.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
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
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867142"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Schválení dodavatelů pro konkrétní kategorie zásobování

[!include [task guide banner](../../includes/task-guide-banner.md)]

V tomto tématu je vysvětleno, jak schválit dodavatele pro určité kategorie zásobování v aplikaci Dynamics 365 for Finance and Operations. Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny. Tento postup popisuje, jak určit, že je dodavatel schválený nebo upřednostňovaný pro specifickou kategorii zásobování. Tento úkol by obvykle prováděl zásobovací pracovník. Tento postup můžete projít v ukázkových datech společnosti USMF.

1. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**.
2. Vyberte dodavatele, kterého chcete nastavit jako schváleného nebo upřednostňovaného dodavatele pro kategorii.
3. V podokně akcí klikněte na možnost **Obecné**.
4. Zvolte **Kategorie**.
5. Zvolte **Přidat kategorii**.
6. V poli **Kategorie** zaškrtněte **KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ**.
7. V poli **Stav kategorie dodavatele** vyberte **Upřednostňované**. Je možné zadat více než jednoho upřednostněného dodavatele pro kategorii.  
8. Zvolte **Uložit**.
9. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Kategorie zásobování**.
10. Ve stromovém zobrazení vyberte **KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI\KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ**.
11. Rozbalte sekci **Dodavatelé**. Zkontrolujte, zda se vámi vybraný dodavatel zobrazí jako upřednostněný dodavatel pro kategorii Kancelářské a stolní příslušenství. Pokud tento postup používáte jako průvodce úkolem, může být nutné zvolit **Odemknout** a umožnit procházení seznamem dodavatelů.  Také je možné přidat upřednostňované a schválené dodavatele na této stránce.  
12. Ve stromové struktuře rozbalte **KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ** a vyberte **Nůžky**.
13. Vyberte **Ne** v poli **Zdědit dodavatele z nadřazené kategorie:**.
14. Vyberte **Ano** v poli **Zdědit dodavatele z nadřazené kategorie:**.

