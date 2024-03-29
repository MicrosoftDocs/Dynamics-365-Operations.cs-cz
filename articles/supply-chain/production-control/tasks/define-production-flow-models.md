---
title: Definování modelů výrobních toků
description: Modely výrobních toků popisují, jak je vypočtena a spravována kapacita pracovních buněk lean manufacturing.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fb12be6f744cee8af3a845d6b278d1f1462ec5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579129"
---
# <a name="define-production-flow-models"></a>Definování modelů výrobních toků

[!include [banner](../../includes/banner.md)]

Modely výrobních toků popisují, jak je vypočtena a spravována kapacita pracovních buněk lean manufacturing. Proto definice modelu výrobního toku je předpokladem definice pracovních buněk. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="define-a-production-flow-model"></a>Definujte model výrobního toku. 
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Modely výrobního toku.
2. Klikněte na položku Nová.
3. V poli model výrobního toku Zadejte ID pro model výrobního toku.
4. Vyberte možnost v poli Typ modelu.
    * Existují dva typy modelu: Propustnost a Hodiny. Pro typ Propustnost bude kapacita pracovních buněk používající tento model výrobního toku vyjádřena a započítána do množství produktu. Pro typ Hodiny bude kapacita pracovních buněk používající tento model výrobního toku vyjádřena a započítána do hodin. Všimněte si, že tuto vlastnost nelze změnit pro existující model výrobního toku. Poté, co pracovní buňky mají rezervace kapacity, nelze typ modelu výrobního toku změnit.  
5. Zadejte počet dní do cyklu EPE.
    * Interval popisuje období, kdy každá část vyrobena ve výrobním toku nebo pracovní buňce bude alespoň jednou vydávána. Čím je kratší cyklus EPE, tím je pružnější výrobní proces. Pokud cyklus EPE = 0, všechny poptávky mohou být vyrobeny v tentýž den. Cyklus EPE se používá pro plánování úloh procesu štíhlé výroby. Když se plánuje úloha na pracovní buňce s cyklem EPE = 5, plánovací proces bude hledat kapacitu pracovní buňky v datu splatnosti – cyklu EPE (5 dní před datem splatnosti) aby bylo zajištěno, že výrobek může být vyroben v tomto cyklu. Doba realizace skladu produktu je obvykle rovna nebo větší než cyklus EPE souvisejícího výrobního procesu.  
6. Vyberte volbu v poli Typ období plánování.
    * Poté, co pracovní buňky mají rezervace kapacity, nelze období plánování změnit. Můžete vybrat pouze modely výrobního toku stejného typu období pro tuto danou pracovní buňku.  
7. V poli Ochranná doba plánování zadejte číslo.
    * Ochranná doba plánování vyjadřuje počet dní, kdy může být provedena rezervace kapacity pro související pracovní buňky. V poli Ochranná doba plánování zadejte počet dní.   Úlohy kanbanových procesů, které se nacházejí mimo toto období, nejsou plánované s automatickým plánováním. Ochranná doba plánování je obvykle dvojnásobná než průměrná skladová doba realizace produktů vyrobených ve výrobním toku nebo pracovní buňce. Cyklus EPE nesmí být větší, než polovina ochranné doby plánování.     
8. V poli Reakce na nedostatek kapacity vyberte možnost.
    * Možnosti obsahují: Odložit – odložení úplné poptávky plánovací události na příští dostupný produkční den, s dostupnou propustností. Zrušit - ukončení automatického plánování pro plánovací událost a ponechání souvisejících prací nenaplánovaných.   Přidat do požadovaného dne - naplánování požadované práce pro požadované období. Tímto dochází k přetížení buňky pro tento den a vyžaduje kontrolu plánovače a ruční interakci.   Rozdělit na dostupná období - rozdělení různých prací plánovací události na všechny dostupné produkční dny, počínaje prvním dostupným dnem. Množství minimální distribuce je množství kanbanové úlohy. Rozdělení přiřadí minimální množství plánování (kanbanové množství) pro každý den s dostatečnou dostupnou propustností.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]