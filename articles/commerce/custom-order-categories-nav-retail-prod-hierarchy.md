---
title: Změna pořadí řazení pro maloobchodní entity
description: Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje v aplikaci Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 67807c53a6ffc6dd09cc6f0e48218e2ee2de559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207768"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Změna pořadí řazení pro maloobchodní entity


[!include [banner](includes/banner.md)]

Maloobchodní prodejci považují vyhledání produktu za primární nástrojem pro interakci se zákazníkem ve všech kanálech. Různé funkce mohou zákazníkům pomoci snadno objevit produkty. Mohou například procházet kategorie, vyhledávat a filtrovat.

Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje. Dále je zde vysvětleno, jak změnit pořadí řazení.

## <a name="overview"></a>Přehled

Podpora třídění různých entit souvisejících s podporou prodeje byla vylepšena. Tato podpora je nyní lépe sladěna se stávajícími scénáři odběratele, které dříve vyžadovaly rozšíření od implementačních partnerů.

Ve verzích Retail starších než 10.0.5 bylo pořadí řazení kategorií v navigační hierarchii abecední. Nová funkce vlastního pořadí řazení umožňuje manažerům podpory prodeje konfigurovat pořadí řazení pro různé entity související s podporou prodeje napříč všemi klienty koncových uživatelů. Mezi tyto klienty patří centrála (HQ) a kontaktní střediska.

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

![Vlastní řazení hierarchie produktů se zápornými hodnotami](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vlastní řazení uvolněných produktů podle kategorie na základě hierarchie produktů](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

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

![Vlastní řazení hierarchie navigace kanálu](./media/ChannelNavCustomSorted.png)

![Vlastní řazení hierarchie navigace katalogu na základě hierarchie navigace kanálu](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS s vlastním řazením kategorií](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Ve výchozím nastavení je funkce vlastního řazení vypnutá. Informace o zapnutí této funkce a dalších funkcí naleznete v tématu [Správa funkcí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]