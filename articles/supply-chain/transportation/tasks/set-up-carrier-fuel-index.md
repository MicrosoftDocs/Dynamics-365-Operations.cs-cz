---
title: Nastavení indexu paliva dopravce
description: Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73336c6803f28239ff8ca78dcff5ea8db0835e32
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146232"
---
# <a name="set-up-a-carrier-fuel-index"></a>Nastavení indexu paliva dopravce

[!include [banner](../../includes/banner.md)]

Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce. Oblast indexu paliva určuje, pro které oblasti má být index paliva použit, a index paliva určuje cenu paliva pro určitý časový úsek. Pokud chcete, aby se projevily změny cen paliva v čase, je možné přiřadit více indexů paliva k dopravci.  Tyto úlohy běžně provádí koordinátor přepravy. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-fuel-index-region"></a>Vytvoření oblasti indexu paliva
1. Přejděte na Správa přepravy > Nastavení > Indexy paliva > Oblasti indexu paliva.
    * Nejprve je třeba vytvořit různé oblasti, které probíhá provoz a výpočet různých palivových příplatků.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Oblast.
4. Zadejte hodnotu do pole Název.
5. Klikněte na položku Uložit.

## <a name="create-a-fuel-index"></a>Vytvoření indexu paliva
1. Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva.
    * Pro nastavené oblasti je nutné zadat aktuální ceny paliva.  
2. Klikněte na položku Nová.
3. V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. V poli Cena za galon zadejte číslo.
6. Zadejte datum a čas do pole Datum a čas platnosti.
7. Klikněte na položku Uložit.

## <a name="create-a-carrier-fuel-index"></a>Vytvoření indexu paliva pro dopravce
1. Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva pro dopravce.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Index paliva dopravce.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klepněte na možnost Nový.
6. Zadejte datum a čas do pole Datum a čas platnosti.
7. V poli Od PPG zadejte číslo.
    * V tomto příkladu nastavíte v poli Od PPG hodnotu 1,95.  
8. Do pole Do PPG zadejte číslo.
    * V tomto příkladu nastavíte v poli Do PPG hodnotu 2.  
9. V poli Procento zadejte požadované číslo.
    * V tomto příkladu nastavíte podíl na hodnotu 3.  
10. V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. Klikněte na položku Uložit.

