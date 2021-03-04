---
title: Vytvoření návrhu odpisování
description: Toto téma popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441247"
---
# <a name="create-a-depreciation-proposal"></a>Vytvoření návrhu odpisování

[!include [banner](../../includes/banner.md)]

Toto téma popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku. Tato úloha používá ukázkovou společnost USMF a účetní role.


## <a name="create-a-depreciation-proposal"></a>Vytvoření návrhu odpisování
1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu**.
2. V poli **Název deníku** vyberte z rozevírací nabídky požadovanou možnost.
3. Do pole **Do data** zadejte datum.

    - Výběrem možnosti **Shrnout odpisy** shrnete měsíční odpisy do jednoho řádku deníku.  
    - Například pokud hodnota Do data je 31. března 2015, vygeneruje se následující popis: "Odpis od 31. ledna 2015." Pole **Datum** na navržených řádcích deníku bude potom nastaveno na 31. března 2015.  
    - Návrhy odpisu mohou být filtrovány podle majetku, skupiny majetku nebo jiných kritérií pomocí možnosti **Filtrování**.  
    - Pokud použijete formulář **Vytvořit návrhy pořízení nebo spotřeby pro dlouhodobý majetek**, můžete navrhnout odpisy v dávkách. To je doporučováno pro větší návrhy, které používají více systémových prostředků. Pokud vyberete možnost dávky, můžete během této doby stále provádět jiné úlohy. Při návrhu odpisu tímto způsobem se počítají odpisy pro oceňovací modely pro dlouhodobý majetek.  

4. Vyberte **Vytvořit deník**.

## <a name="review-depreciation-entries"></a>Zkontrolování položek odpisů
1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Vybrat **řádky**.
4. Zvolte **Zaúčtovat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]