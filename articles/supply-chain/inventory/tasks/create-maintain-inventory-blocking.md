---
title: Vytvoření a správa blokování zásob
description: Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549764"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Vytvoření a správa blokování zásob

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob. Postup můžete spustit s ukázkovými daty společnosti USMF s ukázkovými hodnotami, které jsou zobrazeny. Před zahájením tohoto postupu je třeba mít k dispozici položku s dostupnými fyzickými zásobami na skladě.


## <a name="create-an-inventory-blocking"></a>Vytvoření blokování zásob
1. Přejděte do možnosti Řízení zásob > Periodické úkoly > Blokování zásob.
2. Klikněte na položku Nová.
3. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Ze seznamu vyberte položku, kterou chcete vybrat. 
    * Vyberte číslo položky v rámci fyzických zásob na skladě, kterou chcete blokovat. Pokud používáte USMF, můžete vybrat položku M9201.  
5. Zadejte číslo do pole Množství.
    * Používáte-li položku M9201, musíte vybrat číslo menší než 200.  
6. Rozbalte oddíl Dimenze zásob.
7. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pokud používáte položku M9201, můžete vybrat sklad 51.  
9. Klikněte na položku Uložit.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Aktualizace podmínek pro blokování zásob
1. Zadejte číslo do pole Množství.
    * Aktualizujte pole s množstvím zásob podle blokovaného množství.  
2. V poli Očekávané datum zadejte datum.
    * Můžete určit, zda se u blokovaných zásob očekává uvolnění pro rezervaci přiřazením předpokládaného data. Pokud vyberete možnost Očekávané příjmy pro blokování zásob, zobrazí se toto datum na očekávané transakci, protože se jedná o výchozí údaj při ručním vytváření blokování.  
3. Klikněte na položku Uložit.

## <a name="remove-the-inventory-blocking"></a>Odebrání blokování zásob
1. Klepněte na tlačítko Odstranit.
2. Klepněte na tlačítko Ano.
3. Zavřete stránku.

