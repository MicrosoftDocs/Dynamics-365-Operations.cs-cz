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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

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


