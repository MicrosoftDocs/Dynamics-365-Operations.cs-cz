---
title: Změna pořadí řazení pro maloobchodní entity
description: Tento článek vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265829"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Změna pořadí řazení pro maloobchodní entity


[!Include [banner](includes/banner.md)]

Maloobchodní prodejci považují vyhledání produktu za primární nástrojem pro interakci se zákazníkem ve všech kanálech. Existuje několik funkcí, které mohou zákazníkům pomoci snadno najít produkty. Zákazníci mohou například procházet kategorie, vyhledávat a filtrovat.

Tento článek vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje. Dále je zde vysvětleno, jak změnit pořadí řazení.

## <a name="overview"></a>Přehled

V Commerce je třídění různých entit souvisejících s merchadisingem v souladu se stávajícími scénáři zákazníků a již nevyžaduje rozšíření od implementačních partnerů.

Ve verzích Commerce 10.0.5 a starších bylo pořadí řazení kategorií v navigační hierarchii abecední. Aktuální funkce vlastního pořadí řazení umožňuje manažerům podpory prodeje konfigurovat pořadí řazení pro různé entity související s podporou prodeje napříč všemi klienty koncových uživatelů. Mezi tyto klienty patří centrála (HQ) a kontaktní střediska.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Konfigurace pořadí zobrazení pro kategorie v hierarchii produktů

Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.
2. Klikněte na možnost **Upravit hierarchii kategorií**.
3. Klikněte na možnost **Upravit**.
4. Ve stromovém zobrazení rozbalte **VŠE \> Akční sporty**.
5. Ve stromovém zobrazení rozbalte **VŠE \> Týmové sporty**.
6. Zadejte číslo do pole **Pořadí zobrazení**. (Číslo může být záporné.)
7. Zopakujte kroky 4 až 6 pro všechny další kategorie, u kterých chcete změnit pořadí.

Pořadí zobrazení hierarchie navigace kanálu se odrazí v centrále pro hierarchii produktů commerce a uvolněné produkty podle kategorie.

![Vlastní řazení hierarchie produktů se zápornými hodnotami.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vlastní řazení uvolněných produktů podle kategorie na základě hierarchie produktů.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurace pořadí zobrazení pro kategorie v hierarchii navigace kanálů

Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Navigační kategorie kanálu**.
2. V seznamu vyberte hierarchii navigace **Móda**.
3. Klikněte na možnost **Upravit hierarchii kategorií**.
4. Klikněte na možnost **Upravit**.
5. Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Dámské boty**.
6. Zadejte číslo do pole **Pořadí zobrazení**.
7. Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Halenky**.

Obdobně můžete definovat pořadí řazení pro dílčí kategorie.

8. Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Košile pro volný čas**.
9. Zadejte číslo do pole **Pořadí zobrazení**.
10. Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Kabáty a bundy**.
11. Zadejte číslo do pole **Pořadí zobrazení**.
12. Zopakujte kroky pro všechny další kategorie, u kterých chcete změnit pořadí.

Pořadí zobrazení hierarchie navigace kanálu se odráží v centrále, katalogu a kanálech.

![Vlastní řazení hierarchie navigace kanálu.](./media/ChannelNavCustomSorted.png)

![Vlastní řazení hierarchie navigace katalogu na základě hierarchie navigace kanálu.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS s vlastním řazením kategorií.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Ve výchozím nastavení je funkce **Povolit zobrazení objednávky pro entity merchandisingu** vypnutá. Použijte [Správu funkcí](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k jejímu zapnutí. Po zapnutí funkce spusťte úlohu CDX **Globální konfigurace – 1110** z distribučního seznamu.
> Pokud se vaše pořadí kategorií v POS neaktualizuje, znovu zařízení aktivujte. Informace o kategorii se načítají, když dojde k aktivaci zařízení, takže zařízení může potřebovat znovu načíst informace o kategorii s aktualizovanými objednávkami zobrazení. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
