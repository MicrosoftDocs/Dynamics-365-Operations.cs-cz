---
title: "Změna vlastnictví zásob dodávky na základě výrobní poptávky"
description: "Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c0126ef34ccbf15d180ff9aa474ac7ab8a749bb4
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Změna vlastnictví zásob dodávky na základě výrobní poptávky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě. Tato změna vlastnictví se provádí vytvořením a zaúčtováním deníků změn vlastnictví zásob. Řádky deníku změny vlastnictví lze vytvořit ručně nebo, jak je znázorněno v tomto záznamu, na základě existující výrobní poptávky. Tento úkol obvykle provádí vedoucí dílny. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Používáte-li vlastní data, musí být splněny následující předpoklady: název skladového deníku, který byl nastaven pro změnu vlastnictví zásob, fyzicky zaznamenané zboží na skladě vlastněné dodavatelem a jeden nebo více řádků výrobních zakázek pro materiál. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.


## <a name="create-an-inventory-ownership-journal"></a>Vytvoření deníku vlastnictví zásob
1. Přejděte do nabídky Řízení zásob > Položky deníku > Položky > Změna vlastnictví zásob.
2. Klikněte na položku Nová.
    * Deník změn vlastnictví zásob se používá ke změně vlastníka zásob od dodavatele na stávající právnickou osobu. Tato změna vlastnictví se provádí uvolněním zásob na skladě, které jsou ve vlastnictví dodavatele, a následným přijetím těchto zásob v aktuální právnické osobě.  
3. V poli Název zadejte nebo vyberte hodnotu.
    * Můžete vybrat pouze názvy skladového deníku, které mají typ deníku Změna vlastnictví.  
4. Klikněte na tlačítko OK.
5. Klepněte na možnost Funkce.
6. Klikněte na Vytvořit řádky deníku z výrobních zakázek.
    * Proces změny vlastnictví proces lze spustit pomocí dotazu na všechny výrobní linky, které mají požadavek na spotřebu surovin.  
7. V poli Stavy skladového výdeje k zahrnutí vyberte možnost.
    * Tato možnost umožňuje filtrovat podle stavu problému skladových transakcí. Můžete například vytvořit řádky deníku pro zásoby, které mají fyzické stavy Vydané a Rezervované.  
8. Rozbalte oddíl Záznamy k zahrnutí.
    * Tato část umožňuje aplikovat další filtrování. Můžete například vybrat konkrétní datum surovin.  
9. Klikněte na tlačítko OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Zaúčtování deníku změn vlastnictví zásob
1. Klikněte na položku Zaúčtovat.
    * Při zaúčtování deníku jsou vydány zásoby vlastněné dodavatelem pomocí reference Změna vlastnictví. Zásoby jsou pak přijaty jako zásoby na skladě pomocí skladové transakce, která je aktualizována příjemkou produktu na nákupní objednávce. Všimněte si, že jsou vytvořeny pouze transakce, které se vztahují k zaúčtovanému deníku. Nejsou vytvořeny žádné očekávané skladové transakce.  
2. Klikněte na tlačítko OK.
3. Zavřete stránku.
