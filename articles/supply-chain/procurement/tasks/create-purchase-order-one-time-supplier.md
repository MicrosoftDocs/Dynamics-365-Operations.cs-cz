--- 
title: "Vytvoření nákupní objednávky pro jednorázového dodavatele"
description: "Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele. Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele. Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Vyberte možnost v poli Jednorázový dodavatel.
    * Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky. Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.  
4. Do pole Název zadejte název dodavatele.
5. Klikněte na tlačítko OK.
    * Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku. Neexistují žádné zvláštní vlastnosti související se způsobem provedení. Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována. Nakonec bude účet dodavatele odstraněn. To se provádí obvykle v oddělení závazků.  


