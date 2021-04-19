---
title: Vytvoření nákupní objednávky pro jednorázového dodavatele
description: Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812364"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele. Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele. Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Vytvoření nákupní objednávky pro jednorázového dodavatele
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Vyberte možnost v poli Jednorázový dodavatel.
    * Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky. Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.  
4. Do pole Název zadejte název dodavatele.
5. Klikněte na tlačítko OK.
    * Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku. Neexistují žádné zvláštní vlastnosti související se způsobem provedení. Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]