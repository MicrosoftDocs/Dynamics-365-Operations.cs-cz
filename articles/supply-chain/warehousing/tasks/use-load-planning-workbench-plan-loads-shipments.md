---
title: Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení
description: Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c37a98a3728cb1233a6e1207975a6b8f23f8120d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424193"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení

[!include [banner](../../includes/banner.md)]

Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku. Jako nutnou podmínku si nejprve vytvoříte prodejní objednávku. Tento postup je součástí každodenní práce koordinátora přepravy. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte účet **US-004**.
5. Vyberte **OK**.
6. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyberte položku **A0001**. **A0001** je povoleno pro správu přepravy.  
8. V poli **Pracoviště** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání a potom vyberte položku.
9. Zadejte číslo do pole **Množství**.
10. Do pole **Sklad** zadejte v tomto příkladu '24'. Tento sklad jej povolen pro správu přepravy a rozšířenou správu skladu.  
11. Zvolte **Uložit**.
12. Zavřete stránku.

## <a name="create-a-new-load"></a>Vytvoření nového vytížení
1. Přejděte na **Navigační podokno > Moduly > Správa přepravy > Plánování > Pracovní plocha plánování vytížení**.
2. Vyberte kartu **Řádky prodeje**. Nyní budete vytvářet vytížení pro prodejní objednávku, kterou jste právě vytvořili. Vytížení lze vytvořit podle nabídky a poptávky z nákupních objednávek, převodních příkazů a prodejních objednávek.  
3. V podokně akcí klikněte na možnost **Nabídka a poptávka**.
4. Vyberte **Do nového vytížení**.
5. V poli **ID šablony nákladu** vyberte tlačítko rozevíracího seznamu a otevřete vyhledávání. Šablona vytížení definuje maximální měření pro hmotnost a objem celého vytížení. Šablona vytížení může například představovat velikost kontejneru nebo nákladního automobilu. Vyberte položku.
6. Vyberte **OK**.

## <a name="rate-and-route-the-load"></a>Hodnocení a směrování vytížení
1. Vyberte **Hodnocení a směrování**.
2. Vyberte **Pracovní plocha sazeb trasy**.
3. Vyberte **Sazba – obchod**.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Vyberte **Přiřadit**.
6. Zavřete stránku.

