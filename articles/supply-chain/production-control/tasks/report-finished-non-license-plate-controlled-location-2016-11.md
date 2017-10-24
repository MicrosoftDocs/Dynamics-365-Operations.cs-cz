--- 
title: "Ohlášení jako dokončené pro skladové místo bez řízení na základě registračních značek "
description: "Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>Ohlášení jako dokončené pro skladové místo bez řízení na základě registračních značek  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou. Předpokladem pro tento úkol je příslušné pracovní pravidlo. Předchozí průvodce úlohou popisoval nastavení pracovních zásad. Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.




## <a name="set-up-an-output-location"></a>Nastavení výstupního umístění
1. Přejděte na nabídce Správa organizace > Zdroje > Skupiny prostředků.
2. V seznamu vyberte skupinu prostředků '5102'.
3. Klikněte na možnost Upravit.
4. V poli Výstupní sklad vyberte 51.
5. V poli Výstupní umístění vyberte 001.
    * Umístění 001 není umístění řízené registrační značkou. Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Vytvoření výrobní zakázky a její ohlášení jako dokončené
1. Zavřete stránku.
2. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
3. Klikněte na možnost Nová výrobní zakázka.
4. V poli Číslo zboží zadejte 'L0101'.
5. Klepněte na volbu Nový.
6. V podokně akcí klikněte na možnost Výrobní zakázka.
7. Klepněte na Odhad.
8. Klepněte na tlačítko OK.
9. Klepněte na tlačítko Start.
10. Klepněte na kartuObecné.
11. V poli Automatická spotřeba kusovníku vyberte hodnotu „Nikdy“.
12. Klepněte na tlačítko OK.
13. Klepněte na možnost Vykázat jako dokončené.
14. Klepněte na kartuObecné.
15. Vyberte možnost Ano v poli Akceptovat chybu.
16. Klepněte na tlačítko OK.
17. V podokně akcí klikněte na možnost Sklad.
18. Klepněte na tlačítko Podrobnosti práce.
    * Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena. K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.  


