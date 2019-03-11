---
title: Vytvořit návrh odpisu
description: Tento postup popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "361284"
---
# <a name="create-depreciation-proposal"></a>Vytvořit návrh odpisu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku. Tato úloha používá ukázkovou společnost USMF a účetní role.


## <a name="create-depreciation-proposal"></a>Vytvořit návrh odpisu
1. Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.
2. V poli Název deníku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Do pole Do data zadejte datum.
    * Výběrem možnosti Shrnout odpisy shrnete měsíční odpisy do jednoho řádku deníku.  
    * Například pokud hodnota Do data je 31. března 2015, vygeneruje se následující popis: Odpis od 31. ledna 2015. Pole data na navržených řádcích deníku bude potom nastaveno na 31. března 2015.  
    * Návrhy odpisu mohou být filtrovány podle majetku, skupiny majetku nebo jiných kritérií pomocí možnosti Filtrování.  
    * Pokud použijete formulář Vytvořit návrhy pořízení nebo spotřeby pro dlouhodobý majetek, můžete navrhnout odpisy v dávkách. To je doporučováno pro větší návrhy, které používají více systémových prostředků. Pokud vyberete možnost dávky, můžete během této doby stále provádět jiné úlohy. Při návrhu odpisu tímto způsobem se počítají odpisy pro oceňovací modely pro dlouhodobý majetek.  
5. Klikněte na Vytvoří deník.

## <a name="review-depreciation-entries"></a>Zkontrolování položek odpisů
1. Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na položku Řádky.
4. Klikněte na položku Zaúčtovat.

