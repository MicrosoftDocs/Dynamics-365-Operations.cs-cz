---
title: Vytvoření a správa blokování zásob
description: Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12c6e047e15aaab157e6de70f4a09f500af2965f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424079"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Vytvoření a správa blokování zásob

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob. Postup můžete spustit s ukázkovými daty společnosti USMF s ukázkovými hodnotami, které jsou zobrazeny. Před zahájením tohoto postupu je třeba mít k dispozici položku s dostupnými fyzickými zásobami na skladě.


## <a name="create-an-inventory-blocking"></a>Vytvoření blokování zásob
1. V **podokně navigace** přejděte na **Moduly > Řízení zásob > Periodické úlohy > Blokování zásob**.
2. Klepněte na možnost **Nový**.
3. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Ze seznamu vyberte položku, kterou chcete vybrat. Vyberte číslo položky v rámci fyzických zásob na skladě, kterou chcete blokovat. Pokud používáte USMF, můžete vybrat položku M9201.  
5. Zadejte číslo do pole **Množství**. Používáte-li položku M9201, musíte vybrat číslo menší než 200.
6. Rozbalte záložku s náhledem **Dimenze zásob**.
7. V poli **Sklad** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Pokud používáte položku M9201, můžete vybrat sklad 51.  
9. Klikněte na možnost **Uložit**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Aktualizace podmínek pro blokování zásob
1. Na záložce s náhledem **Obecné** zadejte do pole **Množství** hodnotu. Aktualizujte pole s množstvím zásob podle blokovaného množství.  
2. V poli **Očekávané datum** zadejte datum. Můžete určit, zda se u blokovaných zásob očekává uvolnění pro rezervaci přiřazením předpokládaného data. Pokud vyberete možnost Očekávané příjmy pro blokování zásob, zobrazí se toto datum na očekávané transakci, protože se jedná o výchozí údaj při ručním vytváření blokování.  
3. Klikněte na možnost **Uložit**.

## <a name="remove-the-inventory-blocking"></a>Odebrání blokování zásob
1. V **podokně akcí** klikněte na **Odstranit**.
2. Klepněte na tlačítko **Ano**.
3. Zavřete stránku.

