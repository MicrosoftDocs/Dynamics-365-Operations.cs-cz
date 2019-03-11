---
title: Vytvoření nákupní objednávky pro jednorázového dodavatele
description: Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beaf6bcbc870e11e74289375611c631306545633
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "312869"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele. Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele. Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Vyberte možnost v poli Jednorázový dodavatel.
    * Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky. Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.  
4. Do pole Název zadejte název dodavatele.
5. Klikněte na tlačítko OK.
    * Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku. Neexistují žádné zvláštní vlastnosti související se způsobem provedení. Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována. Nakonec bude účet dodavatele odstraněn. To se provádí obvykle v oddělení závazků.  

